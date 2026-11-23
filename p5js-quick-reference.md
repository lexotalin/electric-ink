# p5.js Quick Reference Guide

## 1. The Core Engine
Every p5.js sketch requires these two primary functions to run.

```javascript
function setup() {
  // Runs ONCE at the very beginning.
  createCanvas(800, 600); // (width, height)
}

function draw() {
  // Runs FOREVER at 60 frames per second.
  background(245, 242, 237); // Clears the screen each frame
}
```

## 2. Coordinates & Shapes
The canvas grid starts at `(0,0)` in the **top-left corner**. Moving right increases X; moving down increases Y.

```javascript
circle(x, y, diameter);       // Drawn from the center
rect(x, y, width, height);    // Drawn from the top-left corner
line(x1, y1, x2, y2);         // Connects two coordinate points
```

## 3. The Digital Paintbrush
Commands read from top to bottom. Once you set a color or thickness, every shape drawn after it gets that style until you change it. Colors use RGB (Red, Green, Blue) on a scale from `0` to `255`.

```javascript
fill(255, 0, 0);      // Dips brush in Red paint (Inside of shapes)
noFill();             // Removes the inside color (Transparent)
stroke(0, 0, 255);    // Dips brush in Blue paint (Borders/Lines)
noStroke();           // Removes borders entirely
strokeWeight(5);      // Sets border/line thickness to 5 pixels
```

## 4. Interaction & Movement
Use these built-in variables to make your sketch respond to the user.

*   `mouseX` / `mouseY` : Current position of the cursor.
*   `pmouseX` / `pmouseY` : Previous position of the cursor (one frame ago).
*   `mouseIsPressed` : `true` if the user is clicking/touching, `false` if not.

```javascript
// dist() calculates the distance between two points
let distance = dist(x1, y1, x2, y2);

// map() converts a number from one range into another range
// map(value, originalMin, originalMax, newMin, newMax)
let myColor = map(mouseX, 0, 800, 0, 255);
```

## 5. Loops, Vertices & Noise (Generative Art)
Instead of drawing standard shapes, you can plot individual points (`vertex`) inside a loop to create complex, continuous paths.

```javascript
beginShape();
for (let x = 0; x < width; x += 10) {
  // noise() creates smooth, organic waves (unlike random() which is jagged)
  let y = noise(x * 0.05) * 100; 
  vertex(x, y); 
}
endShape();
```

## 6. Exporting Vectors and Loading Fonts
Vector Export for Plotters \
Note: for p5.js to support SVG rendering out of the box we use version 1.6.0
```javascript
createCanvas(800, 800, 'SVG'); // Add 'SVG' to setup to record paths, not pixels.
save("my-art.svg");          // Downloads the vector file to your computer
```

Loading Assets & Generative Type:
```javascript
let customFont;

async function setup() {           // Note the "async" keyword
  createCanvas(800, 600);
  
  // Await the font before doing anything else
  customFont = await loadFont('RobotoMono.ttf'); 
  
  textSize(200); // Set the size BEFORE extracting points!
  
  // Break the text into an array of structural X/Y coordinates
  let points = customFont.textToPoints("PULSE", 100, 300, {
    sampleFactor: 0.3 // Density of the points (higher = more points)
  });
}
```
