# Conceptos básicos de animación

## Sol

    noStroke();

    // the starting size for the sun
    var sunSize = 30; 

    draw = function() {
    
    // the beautiful blue sky
    background(82, 222, 240);
    
    
     // The sun, a little circle on the horizon
    fill(255, 204, 0);
    ellipse(200, 298, sunSize, sunSize);
    
    // The land, blocking half of the sun
    fill(76, 168, 67);
    rect(0, 300, 400, 100);
    
    sunSize = sunSize + 1;
    };

## Sol y nuves

    noStroke();
    var leftX = 123;
    var rightX = 284;
    var sunRadius = 100;
    
    draw = function() {
    background(184, 236, 255);
        
    fill(255, 170, 0);
    ellipse(200, 100, sunRadius, sunRadius);
    
    // clouds 
    fill(255, 255, 255);
    
    // left cloud
    ellipse(leftX, 150, 126, 97);
    ellipse(leftX+62, 150, 70, 60);
    ellipse(leftX-62, 150, 70, 60);
    
    // right cloud
    ellipse(rightX, 100, 126, 97);
    ellipse(rightX+62, 100, 70, 60);
    ellipse(rightX-62, 100, 70, 60);
    
    // move
    leftX += -1;
    rightX++;
    sunRadius += 2;
    };
    
## Estrella fugaz
    
    // triangle
    var x = 50;
    var y = 205;
    var xx = 50;
    var yy = 205;
    
    noStroke ();
    
    draw = function() {
        background(29, 40, 115);
        fill(255, 242, 0);
        
    // star yellow 
    triangle(x + 0 , y -18 , x + 15, y + 10, x - 12, y + 10);
    triangle(x + 13 , y -10 , x + 0, y + 18, x - 12, y + -9);
   
     x += 2;
     y -= 1;
    
    //buildings
        // 1
        fill(41, 37, 37);
        rect(10, 242, 84, 160);
        fill(242, 255, 0);
        rect(25, 262, 20, 20);
        rect(25, 333, 20, 20);
        rect(57, 298, 20, 20);
        
        // 2
        fill(41, 37, 37);
        rect(144, 297, 84, 160);
        fill(242, 255, 0);
        rect(200, 311, 20, 20);
        rect(157, 362, 20, 20);
        rect(157, 313, 20, 20);
        
        // 3
        fill(41, 37, 37);
        rect(279, 279, 84, 160);
        fill(242, 255, 0);
        rect(285, 331, 20, 20);
        rect(330, 333, 20, 20);
        rect(290, 298, 20, 20);
    
        // star white
        fill(250, 247, 247);
        triangle(28, 48, 46, 10, 10, 10);
        triangle(48, 36, 14, 36, 26, -5);
    
    //star red
    fill(255, 0, 0);
    triangle(xx+165, yy+5, xx+146, yy+-48, xx+184, yy+-43);
    triangle(xx+150, yy+-7, xx+185, yy+-1, xx+166, yy+-63);
        
    xx -= 0.5;
    yy -= 1;
    };
