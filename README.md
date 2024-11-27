# Swoleboi: Pose Detection and Repetition Counter

## Overview

Swoleboi is a real-time pose detection and repetition counting application designed to monitor specific exercises like deadlifts. Using a webcam, it analyzes body posture and movements, providing feedback on the stage of the exercise and counting repetitions.

## Features

- **Real-time Pose Detection:** Utilizes MediaPipe to capture and analyze body landmarks.
- **Repetition Counting:** Counts repetitions based on the detected stages of exercise.
- **Probability Display:** Shows the probability of the detected pose class.
- **Custom UI:** Built with Tkinter and CustomTkinter for a dark-themed, custom interface.

## Requirements

- Python 3.x
- Tkinter
- CustomTkinter
- Pandas
- NumPy
- OpenCV
- Pillow
- Mediapipe

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/NitinRwt/MLapp.git
   cd MLapp
   ```

2. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Place the model file:**
   - Ensure `deadlift.pkl` is in the project directory. This file contains the trained model for pose classification.

## Usage

1. **Run the application:**
   ```bash
   python swoleboi.py
   ```

2. **Interface Details:**
   - **STAGE:** Shows the current stage of the exercise (e.g., "up" or "down").
   - **REPS:** Displays the count of repetitions completed.
   - **PROB:** Indicates the probability of the current pose classification.

3. **Reset Counter:**
   - Click the "RESET" button to reset the repetitions counter.

## Configuration

- **Webcam Settings:**
  - The default camera index is set to `3`. Adjust `cv2.VideoCapture(3)` to your correct camera index if needed.

- **Pose Confidence:**
  - Adjust the `min_tracking_confidence` and `min_detection_confidence` in `mp_pose.Pose()` for different detection sensitivity.

## Troubleshooting

- **Camera Issues:**
  - Ensure the correct camera index is used.
  - Verify that the camera is not being accessed by another application.

- **Model Errors:**
  - Ensure `deadlift.pkl` is in the correct location and is not corrupted.

## Contributing

Feel free to fork the repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is open-sourced under the MIT License. See the `LICENSE` file for more details.

## Acknowledgments

- Thanks to the MediaPipe team for their pose detection library.
- Inspired by fitness applications that utilize AI for exercise monitoring.
