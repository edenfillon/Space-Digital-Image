# Space-Digital-Image
Our Group Project

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

//draw all the snowflake-type stars
function drawAllStars3() {
  for (var i = 0; i < 20; i++) {
    moveTo(randomNumber(0, 320), randomNumber(0, 450));
    drawStar3 (randomNumber(5, 15));
  }
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
  moveTo(149, 20);
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
