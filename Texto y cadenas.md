# Texto y cadenas

## Lista de comida

fill(24, 168, 86);
textSize(25);
text("*My Favorite Foods", 30, 40);

fill(163, 80, 80);
textSize(15);
text("1.Cannelloni", 45, 70);
text("2.Pizza", 45, 90);
text("3.Paella", 45, 110);

## Rastrear el ratón

fill(255, 0, 255);

draw = function() {
    background(255, 255, 255);
    var X = mouseX;
    var Y = mouseY;
    var cord = X + "," + Y;
    textSize(20);
    text(cord, mouseX+10, mouseY);
    ellipse(mouseX, mouseY, 12, 12);

};

## Coordenadas del ratón

fill(255, 0, 255);

draw = function() {
    background(255, 255, 255);
    var X = mouseX;
    var Y = mouseY;
    var cord = X + "," + Y;
    textSize(20);
    text(cord, mouseX+10, mouseY);
    ellipse(X, Y, 12, 12);
    
};

## Anuncio

var Name1 = "Rodrigo";
var Name2 = "Rosa";
var Hastag = "#Compartecon";
var Size1 = 35;
var Size2 = 50;

// Text
fill (0, 0, 0);
textSize(27);
text("Comparte una", 39, 38);
fill (255, 0, 0);
textSize(63);
text("Coca Cola", 12, 98);
fill (0, 0, 0);
textSize(27);
text("con...", 39, 125);

// Cans
fill(255, 0, 0);
noStroke();
rotate(28);
rect(176, 95, 94, 165);
rotate(-28);
rotate(-29);
rect(82, 284, 94, 165);
rotate(29);

// Name 1
fill(255, 255, 255);
rotate(-62);
textSize(Size1);
text(Name1, -240, 236);
rotate(62);

// Name 2
rotate(-120);
textSize(Size2);
text(Name2, -429, 140);
rotate(120);

// Hastag
fill(0, 0, 0);
textSize(19);
text(Hastag, 10, 397);
