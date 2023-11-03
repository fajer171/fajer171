- 👋 Hi, I’m @fajer171
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
fajer171/fajer171 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
// Variables to keep track of the state of the game
let isGameActive = true;
let isShootingAllowed = true;

// Plane objects
const playerPlane = {
 x: 100,
 y: 200,
 speed: 5,
 angle: 0,
 size: 50,
 isShooting: false,
 score: 0,
};

const enemyPlane = {
 x: 300,
 y: 100,
 speed: 2,
 angle: 180,
 size: 30,
 isShooting: false,
 score: 0,
};

// Function to handle the movement of the planes
function movePlanes() {
 playerPlane.x += playerPlane.speed * Math.cos(playerPlane.angle * Math.PI / 180);
 playerPlane.y += playerPlane.speed * Math.sin(playerPlane.angle * Math.PI / 180);

 enemyPlane.x += enemyPlane.speed * Math.cos(enemyPlane.angle * Math.PI / 180);
 enemyPlane.y += enemyPlane.speed * Math.sin(enemyPlane.angle * Math.PI / 180);
}

// Function to handle the shooting mechanism
function shoot() {
 // Your implementation here
}

// Function to handle the game loop
function gameLoop() {
 if (isGameActive) {
    movePlanes();

    if (isShootingAllowed) {
      shoot();
    }

    // Your implementation here to handle the collisions, scoring, etc.
 }

 // Request the next frame of the game loop
 requestAnimationFrame(gameLoop);
}

// Start the game loop
gameLoop();
