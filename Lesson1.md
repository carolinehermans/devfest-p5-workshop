# Lesson 1: The Canvas

``` javascript
function setup() {
}

function draw() {
} 
```

This sets up an empty file. Click on the index.html file to see it. But it looks blank! 

``` javascript
function setup() {
  background('pink');
}

function draw() {
} 
```

That looks way smaller than it should. That's because we need to create a canvas to draw on.

``` javascript
function setup() {
  createCanvas(100, 100)
  background('pink');
}

function draw() {
} 
```

Better! Let's make it the size of the whole window:

``` javascript
function setup() {
  createCanvas(window.innerWidth, window.innerHeight)
  background('pink');
}

function draw() {
} 
```

Something to note: (0, 0) is actually in the top left corner.


