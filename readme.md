# Tetris

This code is for a tetris game, written in JavaScript and using the HTML5 canvas element for rendering.

## Code structure

The code consists of several functions that handle different aspects of the game.

### update()

This function is called repeatedly using requestAnimationFrame(), and is responsible for updating the game state and rendering the current frame. It takes the current time as an argument, and uses it to calculate the elapsed time since the last frame in order to update the game state accordingly.

### arenaSweep()

This function is called whenever a row is cleared in the game. It removes the row from the arena and shifts all the rows above it down by one. It also updates the player's score and increases the level if necessary.

### collide()

This function checks whether the current piece collides with any blocks in the arena. It returns true if there is a collision, and false otherwise.

### createMatrix()

This function creates and returns a matrix (an array of arrays) with the specified width and height, filled with zeros.

### createPiece()

This function returns a matrix representing the specified tetris piece.

### draw()

This function is responsible for rendering the current frame. It clears the canvas, and then draws the arena and the current piece on it.

### drawMatrix()

This function draws a matrix on the canvas, with the specified offset.

### merge()

This function merges the current piece into the arena.

### playerDrop()

This function moves the current piece down by one row.

### playerMove()

This function moves the current piece left or right by one column.

### playerRotate()

This function rotates the current piece clockwise.

### Global variables

The code also defines several global variables:

- canvas: a reference to the canvas element in the HTML document.
- context: the canvas rendering context, used for drawing on the canvas.
- level: the current level of the game.
- dropCounter: a counter used to track the elapsed time since the last piece drop.
- dropInterval: the interval at which the pieces should drop, based on the current level.
- lastTime: the time at which the last frame was rendered.
- arena: the matrix representing the game arena.
- player: an object representing the current piece, with properties matrix, pos, and score.
- colors: an array of strings representing the colors of the different tetris pieces.
- pieces: a string containing the letters representing the different tetris pieces.