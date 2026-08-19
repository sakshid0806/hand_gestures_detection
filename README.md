# 🤚 Hand Gesture Detection System

A real-time Hand Gesture Detection system built using Python, OpenCV, and Machine Learning. The project uses a webcam to detect hand movements, identify gestures, and convert them into meaningful commands. It demonstrates Computer Vision, gesture recognition, image processing, and contactless Human-Computer Interaction.

## 📌 Project Overview

The Hand Gesture Detection System is designed to provide a contactless Human-Computer Interaction (HCI) experience. The system captures live video through a webcam, detects the user's hand, analyzes its position and finger movements, and identifies the performed gesture using a trained classification model.

## ⚙️ How It Works

1. **Video Capture** – Captures real-time video using a webcam.
2. **Hand Detection** – Identifies the hand in each frame using MediaPipe-based hand landmark tracking.
3. **Feature Extraction** – Crops and normalizes the hand region, analyzing finger positions and orientation.
4. **Gesture Recognition** – A trained Keras model classifies the extracted hand image into a predefined gesture class.
5. **Output Generation** – Displays the recognized gesture and can be extended to trigger a corresponding action or command.

## 🚀 Key Features

- Real-time hand detection and tracking
- Real-time gesture classification
- Webcam-based input
- Custom data collection pipeline for training new gestures
- Computer Vision-based image processing
- Machine Learning-based gesture recognition
- Contactless interaction

## 🛠️ Technologies Used

- Python 3.10
- OpenCV
- cvzone (Hand Tracking Module)
- MediaPipe
- TensorFlow / Keras
- NumPy

## Project Structure

```
sakshiProject/
├── data/
│   ├── A/              # Captured images for gesture "A"
│   ├── B/              # Captured images for gesture "B"
│   └── C/              # Captured images for gesture "C"
├── Model/
│   ├── keras_model.h5  # Trained classification model
│   └── labels.txt      # Class labels used by the model
├── datacollection.py   # Script to capture and save hand gesture images
├── test.py             # Script to run real-time gesture detection
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sakshid0806/hand_gestures_detection.git
   cd hand_gestures_detection
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate      # Windows
   source .venv/bin/activate   # macOS/Linux
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### 1. Collect gesture data
Run the data collection script to capture and save labeled images of hand gestures via webcam:
```bash
python datacollection.py
```

### 2. Test gesture recognition
Run the test script to see real-time gesture predictions:
```bash
python test.py
```

## 🎯 Applications

This project can be extended for several real-world applications, including:

- Gesture-based computer control
- Touchless interfaces
- Smart home control
- Presentation control
- Accessibility applications
- Gaming interfaces
- Sign language recognition

## 🔮 Future Enhancements

- Add support for a larger number of gestures
- Improve recognition accuracy
- Add voice feedback
- Integrate gesture-controlled applications
- Support full sign-language recognition
- Deploy as a web or desktop application

## 👩‍💻 Project Objective

The main objective of this project is to explore AI, Machine Learning, and Computer Vision by developing a practical system that can understand human hand gestures and provide a natural, touch-free method of interacting with technology.

## Notes

- Requires a working webcam.
- MediaPipe currently officially supports Python 3.8–3.11 on Windows.
- If you run into a `ModuleNotFoundError` for `cv2` or `mediapipe`, make sure your virtual environment is active and the correct interpreter is selected in your IDE.

## License

This project is open source and available for personal and educational use.
