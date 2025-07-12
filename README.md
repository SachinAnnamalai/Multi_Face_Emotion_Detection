# Multi-Face Emotion Detection & Real-Time Dashboard with DeepFace and RealSense

## Overview

This project enables **real-time detection of multiple faces and their emotions** using a depth camera (Intel RealSense), OpenCV, and DeepFace. It also displays a **live emotion statistics dashboard** as a bar chart using matplotlib. The system is designed for applications such as smart attendance, wellbeing monitoring, or as a module in autonomous vehicles (e.g., school shuttles for student authorization and safety).

## Features

- **Multi-face detection**: Detects all faces in the camera frame.
- **Real-time emotion recognition**: Analyzes each face for emotions using DeepFace’s pre-trained models.
- **Emotion statistics dashboard**: Displays a live bar chart of emotion counts (happy, sad, etc.) in a separate window.
- **Threaded processing**: Ensures smooth video feed and fast analysis.
- **Immediate clearing**: Removes emotion labels and resets statistics when no faces are present.

## Demo

![Screenshot of Emotion Detection](docs/screenshot_emotion.png)
![Screenshot of Dashboard](docs/screenshot_dashboard.png)

## Setup

### Prerequisites

- Python 3.8 or later
- Intel RealSense camera (tested with D415/D435)
- Operating system: Windows/Linux/macOS

### Install Dependencies

```bash
pip install opencv-python pyrealsense2 deepface matplotlib mediapipe
```

> **Note:** For GPU acceleration, ensure you have a compatible NVIDIA GPU and install TensorFlow or PyTorch with CUDA support.

### Running the Project

1. Connect your RealSense camera.
2. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
   ```
3. Run the main script:
   ```bash
   python multi_face_emotion_dashboard.py
   ```

## How It Works

1. **Face Detection**:  
   Uses OpenCV to detect all faces in each frame.
2. **Emotion Analysis**:  
   Each face is analyzed by DeepFace for emotion classification (happy, sad, neutral, etc.).
3. **Visualization**:  
   Face rectangles and emotion labels are drawn on the video feed.  
   A separate matplotlib window shows live emotion counts as a bar chart.
4. **Performance**:  
   Threading is used for emotion analysis to keep the video feed smooth and responsive.

## Applications

- **Smart school shuttles**: Authorize students via face recognition (can be extended), monitor wellbeing.
- **Attendance systems**: Capture presence and mood.
- **Retail analytics**: Monitor customer emotions.
- **Wellbeing monitoring**: Track mood trends in groups.

## Customization

- **Face recognition**: Extend with DeepFace’s face recognition features to authorize individuals.
- **Web dashboard**: Swap matplotlib for a web dashboard using Dash or Streamlit.
- **Logging**: Add CSV or database logging for attendance/emotion records.

## Dataset Information

- **Emotion model**: Pre-trained on FER2013 (Kaggle) via DeepFace.
- **No manual dataset setup required**: DeepFace loads models internally.

## Troubleshooting

- If DeepFace reports missing models, ensure you have a stable internet connection on first run.
- For GPU support, verify your CUDA and cuDNN versions match TensorFlow/PyTorch requirements.
- If RealSense camera isn’t detected, check USB connection and camera drivers.

## License

MIT License. See [LICENSE](LICENSE) for details.

## Credits

- [DeepFace](https://github.com/serengil/deepface)
- [OpenCV](https://opencv.org/)
- [Intel RealSense](https://www.intelrealsense.com/)
- [Matplotlib](https://matplotlib.org/)

---

**Built by Raja Annamalai as part of an autonomous school shuttle project.**
