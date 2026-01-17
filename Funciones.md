# Funciones

## Nombre

var Name = function() {
    var textX = random(0, 300);
    var textY = random(0, 300);
    var yourName = "Rodrigo";
    fill(255, 0, 0);
    textSize(30);
    text("Hiiii, " + yourName, textX, textY);

};

Name();
Name();
Name();
Name();

## Topos

var drawMole = function(moleX, moleY) {
    noStroke();
    fill(125, 93, 43);
    ellipse(moleX, moleY, 60, 60); // face
    fill(255, 237, 209);
    ellipse(moleX, moleY+10, 33, 28); 
    fill(0, 0, 0);
    ellipse(moleX-10, moleY-15, 10, 10); // eyes
    ellipse(moleX+10, moleY-15, 10, 10);
    ellipse(moleX, moleY-5, 10, 10); // nose
    ellipse(moleX, moleY+10, 20, 5); // mouth
};

background(52, 168, 83); // green grass
fill(0, 0, 0);
ellipse(200, 200, 100, 30); // holes!
ellipse(70, 119, 100, 30);
ellipse(300, 60, 100, 30);
ellipse(297, 350, 100, 30);

drawMole (203, 162);
drawMole (68,82);
drawMole (300, 35);
drawMole (300, 321);

## Calculadora

var add = function(num1, num2) {
    return num1 + num2;
};
var subtract = function(num1, num2) {
    return num1 - num2;
};
var multiply = function(num1, num2) {
    return num1 * num2;
};
var divide = function(num1, num2) {
    return num1 / num2;
};

fill(255, 0, 0);
text("15 + 3 is " + add(15, 3), 10, 20);
text("15 - 3 is " + subtract(15, 3), 10, 50);
text("15 * 3 is " + multiply(15, 3), 10, 80);
text("15 / 3 is " + divide(15, 3), 10, 110);

text("8 + 4 is " + add(8, 4), 10, 170);
text("8 - 4 is " + subtract(8, 4), 10, 200);
text("8 * 4 is " + multiply(8, 4), 10, 230);
text("8 / 4 is " + divide(8, 4), 10, 260);

## Pecera

var centerX = 200;
var centerY = 100;
var bodyLength = 118;
var bodyHeight = 74;
var tailWidth = bodyLength/4;
var tailHeight = bodyHeight/2;
var bodyColor;
var tailColor;
var eyeColor;

var sx = random(10, 300);
var sy = 318;
var sw = 48;
var sh = 95;

var bX = mouseX;
var bY = mouseY;
var bW = 57;
var bH = bW;

var seaWeed = function (sx, sy, sw, sh) {
    image(getImage("cute/TreeShort"), sx, sy, sw, sh);
};

var Bubble = function (bX, bY, bW, bH) {
    
stroke (255, 255, 255);
fill (138, 195, 255, 100);
ellipse (bX, bY, bW, bH);
};

var drawFish = function (centerX, centerY, bodyLength, bodyHeight, tailWidth, tailHeight, bodyColor, tailColor, eyeColor) {
    // body
fill(bodyColor);
ellipse(centerX, centerY, bodyLength, bodyHeight);
// tail
fill(tailColor);
triangle(centerX-bodyLength/2, centerY,
         centerX-bodyLength/2-tailWidth, centerY-tailHeight,
         centerX-bodyLength/2-tailWidth, centerY+tailHeight);
// eye
fill(eyeColor);
ellipse(centerX+bodyLength/4, centerY, bodyHeight/5, bodyHeight/5);
};

draw = function() {
    background(89, 216, 255);
    stroke(0, 0, 0);

// fish1
drawFish(centerX-100, centerY, bodyLength, bodyHeight, tailWidth, tailHeight, color(143, 0, 199), color(222, 156, 255), color(0, 0, 0));
// fish2
drawFish(centerX-48, centerY+220, bodyLength, bodyHeight, tailWidth, tailHeight-10, color(156, 255, 187), color(49, 166, 77), color(1, 110, 1));
// fish 3
drawFish(centerX+92, centerY+92, bodyLength+10, bodyHeight+10, tailWidth, tailHeight+20, color(255, 0, 30), color(232, 105, 126), color(255, 255, 255));

//Bubble
Bubble (bX, bY, bW, bH);

centerX+=2;
if (centerX>600){
    centerX=-300;
}

mouseClicked = function(){
    bX = mouseX;
    bY = mouseY;
};

// SeaWeed
seaWeed (sx+61, sy, sw, sh);
seaWeed (sx+-33, sy, sw, sh);
seaWeed (sx-107, sy, sw, sh);
seaWeed (sx, sy, sw, sh);

};
