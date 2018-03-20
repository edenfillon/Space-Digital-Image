# Space-Digital-Image
Our Group Project

//calls for functions
makeBackground();
drawAllPlanets();
drawMeteor();
drawSun();
drawAllSunrays();
drawWindow();
drawRocketshipBody(230, 310);

//make background
function makeBackground() {
  penColor("#001133");
  dot(2400);
  penUp();
}

function drawAllPlanets() {
  drawPlanet();
  drawPlanet2();
  drawPlanet3(60, 65, 0, 20);
}

// draws all of the diamond stars
function drawAllStars(amount) {
  for (var i = 0; i < amount; i++) {
    penUp();
    moveTo(randomNumber(20,300),randomNumber(30,400));
    penDown();
    drawStar1(randomNumber(5,25));
    penUp();
  }
}

//Draw one snowflake-type star
function drawStar3(size) {
  penDown();
  penWidth(1);
  penRGB(randomNumber(204, 255), randomNumber(153, 255), randomNumber(0, 255));
  moveForward(size);
  moveBackward(size/2);
  turnLeft(90);
  moveForward(size/2);
  turnRight(180);
  moveForward(size);
  turnLeft(180);
  moveForward(size/2);
  for (var i = 0; i < 8; i++) {
    turnLeft(45);
    moveForward(size/2);
    turnLeft(180);
    moveForward(size/2);
  }
  penUp();
}

// draws a singular diamond star
function drawStar1(size) {
  penRGB(randomNumber(204,255),randomNumber(153,255),randomNumber(0,255));
  turnTo(45);
  drawStarSide(size);
  turnTo(165);
  drawStarSide(size);
  turnTo(225);
  drawStarSide(size);
  turnTo(345);
  drawStarSide(size);
}

//draw all the snowflake-type stars
function drawAllStars3() {
  for (var i = 0; i < 20; i++) {
    moveTo(randomNumber(0, 320), randomNumber(0, 450));
    drawStar3 (randomNumber(5, 15));
  }
}

// draws side of diamond star
function drawStarSide(size) {
  penWidth(2);
  arcLeft(size,size);
}

// draws first planet
function drawPlanet() {
  penUp();
  moveTo(170,380);
  penDown();
  penRGB(150,150,0,1.0);
  dot(53);
  moveTo(144,339);
  penRGB(randomNumber(130,140),randomNumber(150,180),0,1.0);
  turnTo(145);
  penWidth(10);
  arcLeft(30,180);
  moveTo(125,363);
  turnTo(145);
  arcLeft(30,178);
  penUp();
}

//Draw the Third Planet Type
function drawPlanet3(size, red, green, blue) {
  moveTo(4, 231);
 penDown();
 penRGB(red, green, blue);
 dot(size);
 penColor("black");
 penWidth(size/10);
 arcLeft(360, size/2);
 arcRight(180, size/4);
 penUp();
} 

//draw a meteor
function drawMeteor() {
  moveTo(260, 60);
  penDown();
  penColor("#606060");
for (var i = 0; i < 4; i++) {
    dot(13);
  turnLeft(90);
  moveForward(15);
  dot(7);
  moveForward(15);
  dot(9);
  dot(11);
  turnRight(90);
  moveForward(5);
  dot(7);
  } 
  turnRight(90);
for (var i = 0; i < 2; i++) {
  moveForward();
  dot(25);
  moveForward(25);
  dot(25);
  } 
  turnRight(180);
  moveForward(23);
  penRGB(255, 69, 0, ".4");
  dot(60);
  moveForward(23);
  dot(60);
  moveForward(23);
  dot(60);
  penUp();
}

// draws sun
function drawSun() {
  penUp();
  moveTo(10,15);
  penColor("yellow");
  dot(50);
  penUp();
  drawAllSunrays();
}

// draws the rays of the sun
function drawAllSunrays() {
  turnTo(0);
  penWidth(2);
  moveTo(0,80);
  penDown();
  arcRight(160,10);
  turnTo(0);
  arcRight(160,10);
  turnTo(-25);
  arcRight(160,10);
  turnTo(-45);
  arcRight(160,10);
  turnTo(-65);
  arcRight(160,10);
  turnTo(-75);
  arcRight(160,10);
  turnTo(-95);
  arcRight(160,10);
  penUp();
}

//draws the Rocketship Body
function drawRocketshipBody(Xlocation, Ylocation) {
  moveTo(Xlocation, Ylocation);
  turnTo(-30);
  penDown();
  penWidth(10);
  penColor("#660000");
  arcLeft(110, 90);
  turnLeft(70);
  arcLeft(110, 90);
  turnTo(270);
  moveForward();
  dot(20);
  penWidth(38);
  moveForward(95);
  turnTo(0);
  penWidth(25);
  moveForward(27.5);
  turnRight();
  moveForward(83);
  arcRight(180, 5);
  penWidth(13);
  moveForward(100);
  turnTo(180);
  moveForward(3);
  arcLeft(90, 10);
  moveForward(5);
  turnRight(90);
  moveForward(19);
  turnLeft(90);
  moveForward(90);
  turnRight(90);
  moveForward(3);
  turnRight();
  penWidth(19);
  moveForward(80);
}

//draws spaceship window
function drawWindow() {
  moveTo(160,240);
  penRGB(0,0,255,0.2);
  dot(50);
  penUp();
}
