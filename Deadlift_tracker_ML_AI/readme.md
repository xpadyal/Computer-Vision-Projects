# Deadlift Form Tracking App

This project is a real-time deadlift tracking application designed to help users maintain proper form during deadlifts by using computer vision and pose estimation. With features like automated rep counting, angle detection, and form feedback, it acts as a virtual fitness coach, providing live feedback on each rep to improve lifting performance.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Overview
Using OpenCV and MediaPipe, this app tracks a user’s deadlift posture by analyzing their knee, hip, and ankle positions. It calculates the joint angles, detects the current stage of the lift (up or down), and assesses the form based on set thresholds. This application is ideal for fitness enthusiasts looking to improve their lifting form with minimal equipment.

## Features
- **Real-Time Rep Counting**: Automatically counts each deadlift rep, freeing you from manual tracking.
- **Angle-Based Form Assessment**: Calculates the knee-hip-ankle angle to determine the quality of your form.
- **Lift Stage Detection**: Identifies the current stage of the lift (up or down) to ensure consistent tracking.
- **Form Quality Feedback**: Provides live feedback on whether your form is within acceptable angles for a proper lift.

## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/deadlift-tracker.git
    cd deadlift-tracker
    ```

2. Install the required packages:
    ```bash
    pip install opencv-python mediapipe numpy
    ```

3. Ensure you have a webcam connected to your system.

## Usage
1. Run the `deadlift_tracker.py` script:
    ```bash
    python deadlift_tracker.py
    ```

2. The app will start capturing video from your webcam. Perform deadlifts in view of the camera to see real-time feedback on:
   - **Rep Count**
   - **Angle**
   - **Stage (up/down)**
   - **Form Quality (Good/Poor)**

3. Press `q` to quit the application or `r` to reset the rep count.

## How It Works
The app uses MediaPipe's pose estimation model to detect landmarks on the body:
- Calculates the angle between the knee, hip, and ankle to assess form.
- Tracks wrist and knee height to determine the up and down stages of each lift.
- Provides visual feedback on-screen about rep count, stage, form quality, and angle.

## Customization
To adjust angle thresholds or modify form evaluation criteria, edit the code in the `start_tracking()` function. The key parameters are:
- **Angle thresholds**: Modify to customize "Good" and "Poor" form ranges.
- **Rep counting**: Adjust wrist and knee height detection for different ranges of motion.

## Contributing
Contributions are welcome! If you'd like to improve this project, feel free to fork the repository, create a new branch, and submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

