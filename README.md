# Survivor Bird

A simple Android game developed in the style of Flappy Bird. The player's goal is to survive as long as possible by avoiding enemies and achieving a high score.

## Features

- Easy gameplay with touch controls
- Enemy avoidance mechanics
- Score tracking system
- Random enemy positioning
- Collision detection system
- Developed with LibGDX framework

## Technologies

- **Java** - Programming language
- **LibGDX** (v1.11.0) - Game development framework
- **Gradle** - Build system
- **Android SDK** (minSdk: 14, targetSdk: 33)

## Project Structure

```
Survivor-Bird/
├── android/          # Android platform implementation
│   ├── src/          # Android launcher code
│   └── res/          # Android resources (icons, colors, etc.)
├── core/             # Game logic (platform independent)
│   └── src/          # Main game code
├── assets/           # Game assets (images)
│   ├── background.png
│   ├── bird.png
│   └── enemy.png
└── gradle/           # Gradle wrapper files
```

## Installation

### Requirements

- Java JDK 7 or higher
- Android SDK
- Gradle

### Build and Run

1. Clone the project:
```bash
git clone <repository-url>
cd Survivor-Bird
```

2. Set up Android SDK path:
   - Create `local.properties` file or set `ANDROID_HOME` environment variable

3. Build the project:
```bash
./gradlew build
```

4. Run on Android device:
```bash
./gradlew :android:run
```

5. To create APK:
```bash
./gradlew :android:assembleRelease
```

The APK file will be created in `android/build/outputs/apk/release/` directory.

## Gameplay

- Tap the screen to move the bird upward
- Avoid enemies
- Your score increases when you pass each enemy set
- Game ends if you hit the ground or collide with enemies
- Tap the screen when game is over to restart

## Development

### Game States

- `gameState = 0`: Start screen
- `gameState = 1`: Game active
- `gameState = 2`: Game over

### Customization

You can adjust game parameters from variables in `SurvivorBird.java`:

- `numberOfEnemies`: Number of enemies on screen (default: 4)
- `gravity`: Gravity force (default: 0.3f)
- `enemyVelocity`: Enemy movement speed (default: 2)
- `velocity`: Bird jump speed (default: -6)