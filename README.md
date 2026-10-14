# Driver Drowsiness Detection Using OpenCV 

A real-time driver drowsiness detection system that uses computer vision and a Support Vector Machine (SVM) classifier to identify closed eyes and alert the driver when signs of drowsiness are detected.

## Overview

Driver drowsiness is a major road-safety concern. This project uses OpenCV and Haar Cascade classifiers to detect eyes from webcam frames, then uses an SVM model to classify them as open or closed. When drowsiness-related conditions are detected, the system triggers an audible alarm, captures screenshots, and logs alerts.

## Features

- **Real-Time Eye Detection:** Detect eyes using a webcam and Haar Cascade classifiers.
- **Eye State Classification:** Classify detected eyes as open or closed using SVM.
- **Drowsiness Alert:** Trigger an audible alarm when the detection logic identifies potential drowsiness.
- **Screenshot Capture:** Save screenshots during alerts for later review.
- **Alert Logging:** Record detected alert events for analysis.

## Tech Stack

- **Python** — Core programming language
- **OpenCV** — Image processing and eye detection
- **Haar Cascade** — Eye detection
- **Scikit-learn** — SVM model training and classification
- **NumPy** — Numerical operations
- **Pickle** — Saving and loading the trained model

## Project Structure

```text
Driver-Drowsiness-Detection/
├── model_training.ipynb
├── webcam_detection.ipynb
├── models/
├── screenshots/
└── README.md
```

*The structure above is illustrative; adjust it to match the actual files in your repository.*

## How It Works

1. Capture frames from the webcam.
2. Detect the eyes using OpenCV and Haar Cascade.
3. Preprocess the detected eye regions.
4. Classify eye states as open or closed using the trained SVM model.
5. Evaluate the detected eye states over time to identify potential drowsiness.
6. Trigger an alarm and save a screenshot and log entry when the alert conditions are met.

## Future Improvements

- **MediaPipe Face Mesh:** Improve facial landmark detection.
- **Eye Aspect Ratio (EAR):** Use eye landmarks to estimate eye closure.
- **Deep Learning:** Explore CNN-based eye-state classification.
- **Temporal Analysis:** Improve reliability by considering eye closure duration and blink patterns.
- **Performance Optimization:** Improve inference speed and robustness under different lighting conditions.

## Limitations

- Performance may vary with lighting, camera placement, glasses, and face orientation.
- Haar Cascade detection may fail under challenging conditions.
- Eye closure alone does not establish that a driver is drowsy.
- This project is a prototype and should not be relied upon as the sole driver-safety system.

## License

Add a suitable open-source license if you intend to distribute the project publicly.
