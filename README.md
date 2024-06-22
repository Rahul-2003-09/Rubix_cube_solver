# Rubik's Cube Solver

The Rubik's Cube is a 3D combination puzzle invented by Ernő Rubik in 1974. This project presents an efficient step-by-step implementation of a 3x3 Rubik's Cube solver.

### Strengths of Our Solution:
- Single write call for the entire program
- No cube rotation in solving algorithms
- Dynamic programming approach
- Solves any given input in approximately 0.001 seconds
- Uses a maximum of 4 kilobytes of memory space

## How It Works

A Rubik's Cube is considered solved when each side is uniformly one color. Our program accepts six 9-length strings of randomized characters that represent each face of the Rubik's Cube. Each letter is capitalized and symbolizes a color. The solver parses the input into two structures: one tracking the corners and the other tracking the middle edges. It then applies various algorithms to solve the cube systematically from the first layer to the second and third layers. Finally, the program outputs a list of steps that will solve the cube. On average, the program takes approximately 150 moves for a complete solution.

### Moves Representation:

![moves](https://raw.githubusercontent.com/mgia/rubix/master/images/image.png)

## Algorithm

Our solver uses a series of algorithms to solve different parts of the cube. Typically, the edges are solved before the corners of each layer.

Here are the series of steps:

1. **White Cross**:
   ![cube](https://raw.githubusercontent.com/mgia/rubix/master/images/white_cross.png)
   
2. **White Corners**:
   ![cube](https://raw.githubusercontent.com/mgia/rubix/master/images/white_corners.png)
   
3. **Middle Layer**:
   ![cube](https://raw.githubusercontent.com/mgia/rubix/master/images/middle_layer.png)
   
4. **Yellow Cross**:
   ![cube](https://raw.githubusercontent.com/mgia/rubix/master/images/yellow_cross.png)
   
5. **Complete**:
   ![cube](https://raw.githubusercontent.com/mgia/rubix/master/images/complete.png)

Reference: [Rubik's Cube Solving Guide](http://www.rossnazirullah.com/students/images/Rubiks.pdf)

## How to Test

# Clone this repository and navigate to the directory containing the code. Compile the code using the following command:

g++ -o rubik_solver main.cpp
### Here is next step
./rubik_solver.exe GGYGGYGGY WBBWBBWBB OOOOOOOOO RRRRRRRRR WWGWWGWWG YYBYYBYYB

### The output will be a list of steps to solve the cube. An example output:
R R R Ri R


### Also, we have created a test function that you can de-comment to print the co-ordinates of the cube:
test_moves(rubik);

### Here are some other test cases that you can also try:
RRWGGWGGW YOOYBBYBB GGGOOOOOO BRRBRRBRR WWBWWBWWO YYRYYGYYG
GGOGGOYYY BBWBBWRRW OOWOOWOOO YRRYRRRGG GWWGWWRRG BBBBYYBYY
YGYYGYOOO RRRWBWWBW WBROOROOY OGYORRWRR GGGWWWBYB GGGBYBBYB
ROGGGWGRG BWBRBBBYR OBWOOOGOW YBYGRGYBY WRRYWRBWR OYOYYWWGO

```sh
