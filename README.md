# Canvas Game

This is a simple HTML5 Canvas game where balls are added and drop through a series of obstacles into sinks. The balls are influenced by gravity and collide with obstacles in their path. The user can add more balls by clicking a button.

## Table of Contents

1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Setup and Installation](#setup-and-installation)
4. [Usage](#usage)
5. [Code Explanation](#code-explanation)

## Features

- Balls drop from the top of the canvas influenced by gravity.
- Obstacles are arranged in a pyramid shape, causing collisions.
- Sinks are placed at the bottom to stop the balls.
- A button allows the user to add more balls to the canvas.

## Technologies Used

- HTML5
- CSS3
- JavaScript

## Setup and Installation

1. Clone the repository or download the ZIP file.
2. Open `index.html` in your preferred web browser.

## Usage

1. Open the `index.html` file in your web browser.
2. Click the "Add Ball" button to add more balls to the canvas.

## Code Explanation

### HTML Structure

- The HTML file contains a `<canvas>` element for drawing the game and a `<div>` element for the "Add Ball" button.
- The canvas has an ID of `gameCanvas` and dimensions of 800x800 pixels.

### CSS Styling

- The canvas background is set to black.
- The "Add Ball" button is styled with a green background and positioned at the top right of the page.

### JavaScript Logic

#### Constants and Variables

- `DECIMAL_MULTIPLIER`: Used to pad values for precision.
- `WIDTH` and `HEIGHT`: Dimensions of the canvas.
- `ballRadius`: Radius of the balls.
- `obstacleRadius`: Radius of the obstacles.
- `gravity`, `horizontalFriction`, `verticalFriction`: Constants influencing the ball's motion.
- `balls`, `obstacles`, `sinks`: Arrays holding the balls, obstacles, and sinks, respectively.

#### Functions

- **pad(n)**: Multiplies a number by `DECIMAL_MULTIPLIER` for precision.
- **unpad(n)**: Divides a number by `DECIMAL_MULTIPLIER` to revert to its original value.

#### Creating Obstacles and Sinks

- Obstacles are created in a pyramid shape with increasing rows.
- Sinks are created at the bottom of the canvas to stop the balls.

#### Ball Class

- **constructor(x, y, radius, color)**: Initializes a ball with position, radius, color, and velocity.
- **draw()**: Draws the ball on the canvas.
- **update()**: Updates the ball's position and handles collisions with obstacles and sinks.

#### Drawing Functions

- **drawObstacles()**: Draws all obstacles on the canvas.
- **drawSinks()**: Draws all sinks on the canvas.

#### Event Listeners

- The "Add Ball" button adds a new ball to the canvas when clicked.

#### Game Loop

- **draw()**: Clears the canvas, draws obstacles, sinks, and updates balls.
- **update()**: Continuously calls the `draw` function using `requestAnimationFrame` for smooth animation
