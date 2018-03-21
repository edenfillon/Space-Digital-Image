# Space-Digital-Image
Our Group Project

//calls for functions
makeBackground();
drawAllStars(10);
drawAllStars2();
drawAllStars3();
drawAllPlanets();
drawMeteor();
drawSun();
drawAllSunrays();
turnTo(90);
drawAlien();
drawWindow();
drawRocketshipBody(230, 310);
drawAlienFace();
hide(); 

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

// draws all of the diamond stars, Eden
function drawAllStars(amount) {
  for (var i = 0; i < amount; i++) {
    penUp();
    moveTo(randomNumber(20,300),randomNumber(30,400));
    penDown();
    drawStar1(randomNumber(5,25));
    penUp();
  }
}

function drawAllStars2 (){
for(var i = 0; i < randomNumber(5,15); i++){
  penUp();
moveTo(randomNumber(10,300),randomNumber(400,0));
penDown();
drawStar2(randomNumber(5,10),randomNumber(204,256),randomNumber(153,256),randomNumber(0,255));
penUp();
 }
} 

//Draw one snowflake-type star, Tara
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

//Draws Cris Crossy Star, Skylla
function drawStar2(size){
  penRGB(randomNumber(204,255),randomNumber(153,255),randomNumber(0,255),1);
  for(var i = 0; i < 5; i++){
    moveForward(size);
    turnRight(145);
  }
  turnTo(90);
}

// draws a singular diamond star, Eden
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

//draw all the snowflake-type stars, Tara
function drawAllStars3() {
  for (var i = 0; i < 20; i++) {
    moveTo(randomNumber(0, 320), randomNumber(0, 450));
    drawStar3 (randomNumber(5, 15));
  }
}

// draws side of diamond star, Eden
function drawStarSide(size) {
  penWidth(2);
  arcLeft(size,size);
}

// draws first planet, Eden
function drawPlanet() {
  penUp();
  moveTo(170,380);
  penDown();
  penRGB(150,150,0,1.0);
  dot(53);
  moveTo(144,339);
  penRGB(130,180,0,1.0);
  turnTo(145);
  penWidth(10);
  arcLeft(30,180);
  moveTo(125,363);
  turnTo(145);
  arcLeft(30,178);
  penUp();
}

//draws second planet, Skylla
function drawPlanet2(){
  moveTo(240,200);
  penColor("#dd8888");
  dot(33);
}


//Draw the Third Planet Type, Tara
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

//draw a meteor, Tara
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

// draws sun, Eden
function drawSun() {
  penUp();
  moveTo(10,15);
  penColor("yellow");
  dot(50);
  penUp();
  drawAllSunrays();
}

// draws the rays of the sun, Eden
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

//draws the Rocketship Body, Tara
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
  penUp();
}

//draws spaceship window, Eden
function drawWindow() {
  moveTo(160,240);
  penRGB(0,0,255,0.2);
  dot(50);
  penUp();
}
//draws alien body, Skylla
function drawAlien(){
   moveTo(160,270);
   penColor("Green");
  dot(20);
  moveTo(160,235);
  penColor("#00b33c");
  dot(20);
  moveTo(176.5,235);
  turnRight(120);
  penWidth(10);
  penDown();
  moveForward(30);
  turnRight(110);
  moveForward(20);
  penUp();
  
}
//draws the alien face, Skylla
function drawAlienFace(){
   moveTo (150,235);
  penColor("black");
  dot(5);
  moveTo(170,235);
  dot(5);
  moveTo(150,247);
  penWidth(2);
  penDown();
  turnTo(180);
  arcLeft(180,10);
  penUp();
  moveTo(160,242.5);
  dot(1);
}
