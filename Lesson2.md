# Lesson 2: Shapes!

Now you have a background, let's draw something on it. We'll start with our code from the end of lesson 1:

``` javascript
void setup() {
  createCanvas(window.innerWidth, window.innerHeight)
  background('pink');
}

void draw() {
} 
```

Let's add a circle.

``` javascript
void setup() {
  createCanvas(window.innerWidth, window.innerHeight)
  background('pink');
}

void draw() {
  ellipse(0, 0, 100, 100);
} 
```

Ooh, that circle looks really cut off. Remember when we said it was in the top left corner?
Let's put it in the middle.

``` javascript
void setup() {
  createCanvas(window.innerWidth, window.innerHeight)
  background('pink');
}

void draw() {
  ellipse(window.innerWidth/2, window.innerHeight/2, 100, 100);
} 
```

What if we want to draw a rectangle?


``` javascript
void setup() {
  createCanvas(window.innerWidth, window.innerHeight)
  background('pink');
}

void draw() {
  rect(window.innerWidth/2, window.innerHeight/2, 100, 100);
} 
```

It looks kind of ugly. Let's play with the colors a bit. Play around with the colors of your circle! They can be anything! Your circle can even become a rectangle! You can also use an RGB color picker.

``` javascript
function setup() {
	createCanvas(window.innerWidth, window.innerHeight);
	background('black');

}

function draw() {
	fill('green');
	stroke('pink');
	strokeWeight(2);
	rect(window.innerWidth/2, window.innerHeight/2, 100, 100);
}
```

