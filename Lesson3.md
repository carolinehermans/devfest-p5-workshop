# Lesson 3: Interactivity!

Let's make this a bit more interesting. We're going to make your shape follow your mouse around.

Starting with our code from last time:

```javascript
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

Now, let's use an *event.* Events are things that happen to the window while it's open. You can handle events inside of your code, and use them to control the contents of your canvas.
Let's replace our X coordinate and our Y coordinate with the X and Y coordinate of your mouse.

That draws a lot of rectangles ALL OVER THE PLACE! What if we just want one?

```javascript
function setup() {
	createCanvas(window.innerWidth, window.innerHeight);

}

function draw() {
	fill('green');
	stroke(0, 0, 255);
	strokeWeight(2);
	background('black');
	rect(mouseX, mouseY, 100, 100);
}
```

Aah, now it draws the background every time. 

Minor nitpick: if you want your shape to be in the center of your mouse, you can fix it by changing the starting X and Y coordinate.

```javascript
function setup() {
	createCanvas(window.innerWidth, window.innerHeight);

}

function draw() {
	fill('green');
	stroke(0, 0, 255);
	strokeWeight(2);
	background('black');
	rect(mouseX - 50, mouseY - 50, 100, 100);
}
```

Let's add in some more events. What about clicks?

```javascript
function setup() {
	createCanvas(window.innerWidth, window.innerHeight);

}

function draw() {
	fill('green');
	stroke(0, 0, 255);
	strokeWeight(2);
	background('black');
	if (mouseIsPressed) { 
		rect(mouseX - 50, mouseY - 50, 100, 100);
	} else {
		ellipse(mouseX, mouseY, 100, 100);
	}
}
```

Let's do one more thing. Let's say "hi!" if a key is pressed.

```javascript
function setup() {
	createCanvas(window.innerWidth, window.innerHeight);

}

function draw() {
	fill('green');
	stroke(0, 0, 255);
	strokeWeight(2);
	background('black');
	if (mouseIsPressed) { 
		rect(mouseX - 50, mouseY - 50, 100, 100);
	} else {
		fill('red');
		ellipse(mouseX, mouseY, 100, 100);
	}

	if (keyIsPressed) {
		background('white');
		fill('black');
		textSize(100);
		text('Hi!', mouseX, mouseY);
	}
}
```

You can even make a little drawing app that draws blue when no key is pressed and red when a key is pressed.

```javascript
function setup() {
	createCanvas(window.innerWidth, window.innerHeight);
	background('black');
}

function draw() {
	fill('green');
	stroke(0, 0, 0);
	strokeWeight(2);
	

	var shapeW = 10;
	var shapeH = 10;

	if (keyIsPressed) { 
		fill('red');
	} else {
		fill('blue');
		
	}

	ellipse(mouseX, mouseY, shapeW, shapeH);
}
```



