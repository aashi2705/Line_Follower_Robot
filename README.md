# Line_Follower_Robot

Overview:  
This project implements a basic line-following robot using Arduino. The robot follows a line on the ground using two IR sensors and controls the direction and speed of two DC motors. Based on sensor readings, the robot moves straight, turns left, turns right, or stops to stay aligned with the track.

Features:
- Line Following: Uses two IR sensors to detect the line and guide the robot.
- Motor Direction Control: Controls left and right motor direction using digital output pins.
- PWM Speed Control: Uses PWM signals to drive both motors at controlled speed.
- Sharp Turning Logic: Makes corrective turns by rotating one motor forward and the other backward.
- Simple and Modular Code: Uses a separate `rotateMotor()` function for cleaner implementation.

Components:
- Arduino Uno
- Motor Driver Module
- 2 DC Motors
- 2 IR Sensors
- Robot Chassis and Wheels
- Power Supply / Battery Pack

Code Explanation:
- `setup()`: Initializes motor control pins and IR sensor pins. It also changes the PWM frequency for smoother motor behavior at lower speed.
- `loop()`: Continuously reads the left and right IR sensor values and decides whether the robot should move straight, turn left, turn right, or stop.
- `rotateMotor()`: Controls motor direction and speed for both motors based on the values passed to it. Positive speed moves a motor forward, negative speed moves it backward, and zero stops it.

Working Logic:
- When both sensors read LOW, the robot moves straight.
- When the right sensor reads HIGH and the left sensor reads LOW, the robot turns right.
- When the left sensor reads HIGH and the right sensor reads LOW, the robot turns left.
- When both sensors read HIGH, the robot stops.
