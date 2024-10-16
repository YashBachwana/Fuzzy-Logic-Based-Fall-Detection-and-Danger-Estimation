# Fuzzy Logic Based Fall Detection and Danger Estimation App

This project implements a Fuzzy Logic-based Android/iOS app that monitors accelerometer data to detect falls and assess the level of danger using sound and motion data. If the danger level is high, the app sends an alert with the GPS location and sound recording to another phone.

## Features
1. **Fall Detection**: Monitors the accelerometer data to detect falls when the app is ON.
2. **Microphone Activation**: Automatically switches ON the microphone upon detecting a fall and measures the sound level.
3. **Fuzzy Logic Danger Assessment**: Uses fuzzy logic to estimate the level of danger based on sound levels and accelerometer data:
    - **Sound Levels**: Low, Medium, High.
    - **Accelerometer Levels**: Low, Medium, High.
    - **Danger Levels**: Low, Medium, High.
4. **Alert System**: If the danger level is High:
    - Sends an alert to a parent’s phone using TCP/IP or UDP.
    - Transmits the recorded sound and the GPS location of the child's phone.
5. **Buzzer Sound**: Plays a buzzer on the first phone (child's phone):
    - The buzzer volume is proportional to the assessed danger level.
    - Activated for both Medium and High danger levels.

## Project Files
- `child.slx`: This file contains the Simulink model for the child's phone, which monitors fall detection, assesses danger, and manages alerts.
- `parent.slx`: This file contains the Simulink model for the parent’s phone, which receives alerts and handles incoming data.

## Demonstration Video
Watch the video demonstration of the project: [Fall Detection App Demo](https://www.youtube.com/watch?v=B4AKJSLjLeE)
