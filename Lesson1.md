# Lesson 1: The Canvas

``` javascript
void setup() {
}

void draw() {
} 
```

This sets up an empty file. Click on the index.html file to see it. But it looks blank! 

``` javascript
void setup() {
  background('pink');
}

void draw() {
} 
```

That looks way smaller than it should. That's because we need to create a canvas to draw on.

``` javascript
void setup() {
  createCanvas(100, 100)
  background('pink');
}

void draw() {
} 
```

Better! Let's make it the size of the whole window:

``` javascript
void setup() {
  createCanvas(window.innerWidth, window.innerHeight)
  background('pink');
}

void draw() {
} 
```

Something to note: (0, 0) is actually in the top left corner.


