# Canvas Drawing Program using NodeJS
This is menu driven console version of canvas drawing program using NodeJS.

Currently, the program should work as follows:
 Upon running the program user will see the main menu as :-
<br/><br/><<------MENU------>>
<br/><1> Create a new canvas
<br/><2> Start drawing on the canvas by issuing various commands
<br/><3> Quit
<br/><br/>Then program will ask for user interest, and proceed with further canvas drawing commands (operations).
<br/>

## Supported canvas drawing commands - 
<br/>Below are the supported commands for canvas drawing operations.
-  'C w h' -- Create a new canvas of width w and height h.
-  'L x1 y1 x2 y2' -- Create a new line from (x1,y1) to (x2,y2). Currently only horizontal or vertical lines are supported. Horizontal and vertical line will be drawn using the 'x' character.
-  'R x1 y1 x2 y2' -- Create a new rectangle, whose upper left corner is (x1,y1) and lower right corner is (x2,y2). Horizontal and vertical lines will be drawn using the 'x' character.
-  'B x y c' -- Fill the entire area connected to (x,y) with "colour" c. The behaviour of this is the same as that of the "bucket fill" tool in paint programs.
-  'Q' -- Quit the program.

### Assumptions

- Coordinates indices are based of 1 instead of 0. For example, if you want to draw a line from top left corner of the canvas, the starting point would be (1,1) instead of (0,0). This is done to match the given sample output.
- Currently the program only supports left to right drawing of lines and rectangles. For example, if x1, y1 is greater than x2, y2, the line will not be drawn.
- Only horizontal and vertical lines are supported for now.

### Sample Input/Ouput
Below is a sample run of the program. User input is prefixed with enter command:

```
Enter Command: C 20 4
----------------------
|                    |
|                    |
|                    |
|                    |
----------------------
Enter Command: L 1 2 6 2
----------------------
|                    |
|xxxxxx              |
|                    |
|                    |
----------------------
Enter Command: L 6 2 6 4
----------------------
|                    |
|xxxxxx              |
|     x              |
|     x              |
----------------------
Enter Command: R 16 1 20 3
----------------------
|               xxxxx|
|xxxxxx         x   x|
|     x         xxxxx|
|     x              |
----------------------
Enter Command: b 10 3 o
----------------------
|oooooooooooooooxxxxx|
|xxxxxxooooooooox   x|
|     xoooooooooxxxxx|
|     xoooooooooooooo|
----------------------
```

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

[Node](https://nodejs.org/en/) and [NPM](https://www.npmjs.com/) are required to run the program.

```
node >= v7.10.0
npm  >= v4.2.0
```

### Installing

 - Git clone or download the zip file
 - cd into the folder
 - Run npm install

```
npm install
```
### Running the program

The program is written in ES6. [Babel](https://babeljs.io/) is used to transpile the code to avoid compatibility issues. To run the program, execute the following command


```
npm run build
npm start
```

## Testing

### Running the tests

Unit tests are written using [Jest](http://facebook.github.io/jest/). To execute tests, run:

```
npm test
```
To keep Jest running in the background to watch for file changes, run:
```
npm run test-watch
```

### Code Coverage

Jest comes with default code coverage report. The following command generates reports in a folder named coverage in the project directory.

```
npm run coverage
```



