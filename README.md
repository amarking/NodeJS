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

- As of now, we can able to draw horizontal and vertical lines, diagonal lines not supported.
- Coordinates indices are based of 1 instead of 0. For example, if you want to draw a line from top left corner of the canvas, the starting point would be (1,1) instead of (0,0). This is done to match the given sample output.
- Current implementation supports left to right drawing of lines and rectangles. For example, if x1, y1 is greater than x2, y2, the line will not be drawn.

## Setting up and running the program code --

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Requirements -

```
node >= v7.10.0
npm  >= v4.2.0
```

### Setting up locally

 - Download the zip file
 - cd into the folder
 - Run npm install

```
npm install
```
### Executing the program

To run the program by executing the following command

```
npm run build
npm start
```

## Testing

### Running the tests

Unit tests are written using [Jest]. To execute tests, run:

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
### Sample output of program
Below is a sample run of the program. User input is prefixed with enter command:

```
------------------------------------------------------------------------------
                This is menu driven Canvas drawing program
------------------------------------------------------------------------------



                <<--------MENU-------->>
                <1> Create a new canvas
                <2> Start drawing on the canvas by issuing various commands
                <3> Quit

Please select valid menu option : 1

Please Enter Canvas operation Command : c 20 4

----------------------
|                    |
|                    |
|                    |
|                    |
----------------------


                <<--------MENU-------->>
                <1> Create a new canvas
                <2> Start drawing on the canvas by issuing various commands
                <3> Quit

Please select valid menu option : 2

Please Enter Canvas operation Command : l 1 2 6 2

----------------------
|                    |
|******              |
|                    |
|                    |
----------------------


                <<--------MENU-------->>
                <1> Create a new canvas
                <2> Start drawing on the canvas by issuing various commands
                <3> Quit

Please select valid menu option : 2

Please Enter Canvas operation Command : l 6 3 6 4

----------------------
|                    |
|******              |
|     *              |
|     *              |
----------------------


                <<--------MENU-------->>
                <1> Create a new canvas
                <2> Start drawing on the canvas by issuing various commands
                <3> Quit

Please select valid menu option : 2

Please Enter Canvas operation Command : r 14 1 18 3

----------------------
|             *****  |
|******       *   *  |
|     *       *****  |
|     *              |
----------------------


                <<--------MENU-------->>
                <1> Create a new canvas
                <2> Start drawing on the canvas by issuing various commands
                <3> Quit

Please select valid menu option : 2

Please Enter Canvas operation Command : b 10 3 o

----------------------
|ooooooooooooo*****oo|
|******ooooooo*   *oo|
|     *ooooooo*****oo|
|     *oooooooooooooo|
----------------------


                <<--------MENU-------->>
                <1> Create a new canvas
                <2> Start drawing on the canvas by issuing various commands
                <3> Quit

Please select valid menu option : 2

Please Enter Canvas operation Command : q
----------------------
```



