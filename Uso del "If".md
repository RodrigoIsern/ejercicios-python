# Uso del "If"

## Rebotar

    // position
    var y = 0;
    // speed
    var speed = 2;
    
    draw = function() {
        background(127, 204, 255);
        fill(66, 66, 66);
        ellipse(200, y, 50, 50);
    
        // speed
        y = y + speed;
        
        if (y>375) {speed -=2;}
        if (y<25) {speed +=2;}
    };

## Pintar

    draw = function() {
        noStroke();
        fill(255, 0, 0);
        
        if (mouseIsPressed) {
        ellipse(mouseX, mouseY, 20, 20);
        }
    };

## Análisis

    var theNumber = 0;
    
    fill(0, 0, 0);
    textSize(30);
    text("Analysis of: " + theNumber, 10, 36);
    
    text("It's positive", 10, 90);
    text("It's negative", 10, 140);
    text("It's zero", 10, 190);
    
    noFill();
    if (theNumber > 0) {
        rect(5, 60, 220, 40);
    }
    
    if (theNumber < 0) {
    rect(5, 110, 220, 40);
    }
    
    if (theNumber === 0) {
    rect(5, 160, 220, 40); 
    }

## Boton

    draw = function() {
        fill(0, 255, 68); // start color
        // Red
        if (mouseIsPressed && mouseY <= 200) {
        fill(255, 0, 0);
    }
        rect(0, 0, 400, 200);  // the button
    
        // The button text
        fill(0, 0, 0);
        textSize(30);
        text("Press me!", 145, 115); 
    };

## Boton 2

    draw = function() {
        fill(0, 255, 68); // start color
    
        if (mouseIsPressed && mouseX>50 && mouseX<300 && mouseY>150 && mouseY<250) { 
            fill(33, 112, 52); // click color
        }
        rect(50, 150, 250, 100);  // the button
    
        // The button text
        fill(0, 0, 0);
        textSize(30);
        text("PRESS ME!", 93, 193);
    };

## Tarjeta

    draw = function() {
        background(165, 219, 162);
        fill(255, 254, 222);
        rect(20, 100, 364, 200);
    
        fill(0, 0, 0);
        textSize(20);
    
    if (mouseIsPressed) {
        text("It's JavaScript!!!", 127, 200);
    
    } else {
    
        text("What programming language is this?", 39, 200);
    }
    };
## Bola magica

    fill(0, 0, 0);
    ellipse(200, 200, 375, 375);
    fill(60, 0, 255);
    triangle(200, 75, 310, 280, 94, 280);
    
    var answer = round(random(0, 1));
    if (answer > 0) {
        fill(255, 255, 255);
        textSize(17);
        text("NOT YET", 165, 200);
        text("IMPLEMENTED", 141, 229);
    } else {
        fill(0, 255, 55);
        triangle(200, 75, 310, 280, 94, 280);
        fill(0, 0, 0);
        textSize(17);
        text("IMPLEMENTED", 140, 211); 
    }

