# Plinko with Scores 🎯

A physics-based Plinko game where colorful balls bounce randomly down a pegboard into scoring zones. Drop balls and watch them navigate through blue pegs to land in different point values!

## Features ✨

- **Physics-Based Ball Dropping**: Click anywhere to drop colorful particles
- **Random Ball Colors**: Each ball gets a unique random color
- **Plinko Pegs**: 4 rows of blue pegs create authentic random bouncing
- **Scoring System**: Different point values (100, 200, 500) based on landing zones
- **Game Limit**: 5 balls maximum before "Game Over"
- **Visual Feedback**: Real-time score display and colorful animations

## Tech Stack 🛠️

- **p5.js** - Creative coding library for graphics and animation
- **Matter.js** - 2D physics engine for realistic ball physics
- **HTML5 Canvas** - Game rendering and mouse interaction
- **JavaScript ES6** - Game logic and physics simulation

## Gameplay 🎮

### Objective
Drop colorful balls down the Plinko board and score points based on where they land. Aim for the higher-value zones to maximize your score!

### How to Play
1. **Click**: Click anywhere on the screen to drop a ball
2. **Watch**: Ball bounces randomly off blue pegs as it falls
3. **Score**: Ball lands in scoring zone and adds points to your total
4. **Repeat**: Continue dropping balls (maximum 5 per game)
5. **Game Over**: After 5 balls, game ends and displays final score

### Scoring Zones
- **100 Points**: Outer zones (easier to hit)
- **200 Points**: Middle zones (moderate difficulty)
- **500 Points**: Center zones (highest reward)

## Controls 🕹️

- **Mouse Click**: Drop a ball from the top of the board
- **Random Colors**: Each ball automatically gets a unique color

## Project Structure 📁

\`\`\`
PLINKO/
├── sketch.js              # Main game logic and physics setup
├── Particle.js           # Ball physics and rendering
├── Plinko.js             # Blue peg objects
├── divisions.js          # Scoring zones and walls
├── Ground.js             # Bottom boundary
├── index.html            # HTML entry point
├── libraries/
│   ├── p5.js            # p5.js core library
│   ├── p5.play.js       # Physics objects
│   └── matter.js        # Matter.js physics engine
├── style.css            # Game styling
└── README.md            # This file
\`\`\`

## Installation & Setup 🚀

### Prerequisites
- Modern web browser with HTML5 Canvas support
- Local web server (recommended for asset loading)

### Quick Start

1. **Clone the repository**
   \`\`\`bash
   git clone https://github.com/Ace3r3x/PLINKO.git
   cd PLINKO
   \`\`\`

2. **Run locally**
   \`\`\`bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (if you have http-server installed)
   npx http-server
   
   # Using Live Server (VS Code extension)
   # Right-click index.html -> "Open with Live Server"
   \`\`\`

3. **Play the game**
   - Navigate to `http://localhost:8000`
   - Click anywhere to drop colorful balls
   - Watch them bounce through pegs into scoring zones

## Code Structure 🏗️

### Main Components

**Game Classes**:
- `Particle`: Colorful balls with physics bodies and random colors
- `Plinko`: Blue pegs that balls bounce off
- `Divisions`: Scoring zones with point values
- `Ground`: Bottom boundary for physics

### Physics Implementation

**Ball Creation**:
\`\`\`javascript
// Create colorful balls with random colors
let particle = new Particle(mouseX, 10, 10);
particle.color = color(random(0, 255), random(0, 255), random(0, 255));
\`\`\`

**Peg Layout**:
\`\`\`javascript
// 4 rows of alternating blue pegs
for (let j = 40; j <= height - 200; j += 50) {
    for (let i = 40; i <= width - 50; i += 50) {
        plinkos.push(new Plinko(i, j));
    }
}
\`\`\`

**Scoring System**:
\`\`\`javascript
// Different point values based on landing position
if (particle.body.position.x < 300) {
    score += 100;
} else if (particle.body.position.x < 600) {
    score += 200;
} else {
    score += 500;
}
\`\`\`

## Game Features 🎯

### Physics Simulation
- **Realistic Ball Physics**: Balls bounce authentically off pegs
- **Random Trajectories**: Each drop creates unique paths
- **Gravity Effects**: Natural falling motion with physics
- **Collision Detection**: Accurate peg and wall interactions

### Visual Design
- **Colorful Balls**: Each ball gets random RGB colors
- **Blue Pegs**: Consistent peg design for clear visibility
- **Score Display**: Real-time score updates
- **Clean Layout**: Organized pegboard with clear scoring zones

### Game Mechanics
- **Limited Attempts**: 5 balls maximum per game
- **Progressive Scoring**: Build up points with each successful drop
- **Game Over State**: Clear end condition with final score
- **Random Elements**: Unpredictable ball paths create replayability

## Educational Value 📚

### Physics Concepts
- **Probability**: Random bouncing demonstrates chance outcomes
- **Gravity**: Consistent downward force on all balls
- **Collision Physics**: Elastic collisions with pegs
- **Trajectory Variation**: Small changes create big differences

### Learning Outcomes
- Understanding probability and randomness
- Physics simulation appreciation
- Strategic thinking about optimal drop positions
- Interactive probability experimentation

## Future Enhancements 🔮

- **Fix Scoring Logic**: Handle all 9 scoring zones properly
- **Restart Functionality**: Allow multiple games without refresh
- **Particle Cleanup**: Remove balls after scoring
- **Sound Effects**: Audio feedback for bounces and scoring
- **High Score System**: Track best scores across sessions
- **Multiple Difficulty Levels**: Different peg arrangements
- **Power-ups**: Special balls with unique properties
- **Multiplayer Mode**: Take turns and compare scores

## Known Issues 🔧

- Scoring logic only handles 3 of 9 displayed zones
- No restart mechanism after game over
- Particles remain on screen after scoring
- Duplicate scoring code needs refactoring

## Repository Information 📋

- **Repository**: [Ace3r3x/PLINKO](https://github.com/Ace3r3x/PLINKO)
- **Created**: November 22, 2020
- **Language**: 100% JavaScript
- **Type**: Physics-Based Probability Game

## License 📄

This project is open source and available under the MIT License.

---

**Drop, Bounce, Score! 🎯✨**


