# Tank Game for NIOS II Processor

## Overview
This project is a tank game implemented for the NIOS II processor, utilizing low-level hardware interactions and game logic written in C. The game involves two players controlling tanks, navigating a grid, and shooting projectiles at each other. The game leverages the Altera NIOS II development environment, hardware-mapped registers, and VGA display for rendering.

---

## Features
- **Multiplayer Gameplay**: Two-player mode with tank movement and shooting mechanics.
- **Real-time Rendering**: Graphics displayed on a VGA screen using pixel plotting and line-drawing techniques.
- **Custom Map Design**: Nine predefined maps with walls and obstacles.
- **Collision Detection**: Checks for collisions between tanks, walls, and projectiles.
- **Audio Feedback**: Sound effects for shooting and other actions.
- **Interrupt Handling**: Use of NIOS II interrupts for efficient game loop control.
- **Customization**: Configurable gameplay parameters such as tank speed, rotation, and ammo characteristics.

---

## Hardware Requirements
- Altera NIOS II processor.
- VGA display for graphical output.
- PS/2 keyboard for player controls.
- On-chip SRAM for game logic and buffers.
- SDRAM for extended memory needs.

---

## Software Details
### Key Modules
1. **Graphics Rendering**:
   - Functions for drawing tanks, projectiles, and walls using pixels and lines.
   - Real-time screen clearing and updates.
   - VGA buffer management for smooth rendering.

2. **Game Logic**:
   - Player movement and rotation.
   - Shooting mechanics with ammo tracking.
   - Collision detection and map boundaries.

3. **Input Handling**:
   - Keyboard inputs for player controls using PS/2 interface.
   - Mapped keys for tank movement, rotation, and shooting.

4. **Interrupts and Timers**:
   - Custom interrupt service routines for timer-based game updates.
   - Efficient handling of game states and rendering.

---

## How to Build and Run
1. **Setup Environment**:
   - Install the Altera Quartus and NIOS II IDE.
   - Set up the NIOS II hardware with the necessary peripherals.

2. **Compile the Code**:
   - Load the project into the NIOS II IDE.
   - Compile the C source code.

3. **Deploy**:
   - Flash the compiled binary onto the NIOS II processor.

4. **Play the Game**:
   - Connect a VGA display and keyboard.
   - Use the assigned keys to control the tanks and start playing.

---

## Controls
- **Player A**:
  - Movement: `Arrow Keys`.
  - Shoot: `Enter`.
- **Player B**:
  - Movement: `WASD`.
  - Shoot: `Space`.

---

## Gameplay Parameters
- **Tank Movement Speed**: 1.6 units/frame.
- **Ammo Speed**: 2 units/frame.
- **Ammo Limit**: 3 projectiles per player.
- **Map Dimensions**: 320x240 pixels.

---

## Files and Structure
- **`game.c`**: Main source file containing game logic, rendering, and input handling.
- **`Interrupts.c`**: Contains interrupt and exception handling routines.
- **`Graphics.c`**: Functions for drawing and rendering on the VGA display.
- **`Audio.c`**: Sound playback routines.

---

## Future Enhancements
- Add AI-controlled tanks for single-player mode.
- Implement more dynamic map generation.
- Support for additional hardware like joysticks.
- High-score tracking and more detailed stats display.
