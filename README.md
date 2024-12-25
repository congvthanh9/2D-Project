# HeroNew Assets README

## Overview
This folder contains the exported assets for a character with perfectly integrated basic animations. These animations are designed for smooth transitions and seamless gameplay experiences, making them ideal for platformers, action games, or any 2D side-scrolling project.

### Folder Name
`heronew_<current date>_<current month>`

### Export Date
`<current date>`

## Included Animations
The following animations are included and have been fine-tuned for fluid transitions:

1. **Idle**
   - The default resting animation for the character when no input is detected.

2. **Run**
   - A dynamic running animation triggered when the character moves horizontally.

3. **Jump**
   - An upward movement animation triggered by a jump input. Perfect for vertical traversal and platforming.

4. **Fall**
   - A descending animation that activates after the peak of the jump. This includes parameters for smooth integration when the character lands.

## Setup Instructions
1. **Animator Controller**
   - Ensure the Animator Controller references the animations correctly using the states provided in Unity’s Animator window.
   - States to configure:
     - Idle
     - Run
     - Jump
     - Fall

2. **Parameters**
   - Set up the following Animator parameters to control transitions:
     - `Grounded` (Boolean): Determines if the character is on the ground.
     - `Speed` (Float): Controls the Idle/Run transition based on movement.
     - `AirSpeedY` (Float): Determines the transition from Jump to Fall based on vertical velocity.

3. **Transitions**
   - Transitions have been configured with conditions to ensure animations flow without interruptions:
     - Idle to Run: Triggered by `Speed > 0`.
     - Run to Idle: Triggered by `Speed == 0`.
     - Jump to Fall: Triggered when `AirSpeedY < 0`.
     - Fall to Idle: Triggered by `Grounded == true`.

4. **Physics Integration**
   - Ensure the Rigidbody2D component is configured with appropriate gravity and drag settings to match the animation behavior.

## Usage Notes
- These animations are designed to work together seamlessly. Make sure to test transitions in your specific game environment to adjust timing or conditions if necessary.
- For optimal performance, ensure frame rates and animation curves are consistent across different resolutions and devices.

## Credits
Assets were created and configured using Unity 2D tools. All animations are optimized for reuse and customization.

