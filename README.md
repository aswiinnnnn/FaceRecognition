# Face Recognition System

This project is a Python-based face recognition system using OpenCV, face_recognition, and text-to-speech feedback. It identifies faces from a webcam feed by comparing them to a set of known images and provides audio feedback using Google Text-to-Speech and playsound.

## Features

- Loads known faces from the `Faces/` directory.
- Encodes faces and matches them in real-time using a webcam.
- Provides audio feedback for recognized and unrecognized faces.

## Requirements

- Python 3.9+
- [OpenCV](https://pypi.org/project/opencv-python/) (`cv2`)
- [face_recognition](https://pypi.org/project/face-recognition/)
- [dlib](https://pypi.org/project/dlib/) (required by face_recognition)
- [numpy](https://pypi.org/project/numpy/)
- [playsound==1.2.2](https://pypi.org/project/playsound/)
- [gTTS](https://pypi.org/project/gTTS/)
- Visual Studio Code (recommended for running Jupyter notebooks)

## Installation

### 1. Install Python Modules

Install all dependencies using pip:

```sh
pip install opencv-python face_recognition numpy playsound==1.2.2 gTTS
```

### 2. Install dlib

`face_recognition` depends on `dlib`, which may require CMake and Visual Studio Build Tools on Windows. If you encounter installation issues, follow these steps:

- Install CMake:
  ```sh
  pip install cmake
  ```
- Install Visual Studio Build Tools from [here](https://visualstudio.microsoft.com/visual-cpp-build-tools/).
- Then install dlib:
  ```sh
  pip install dlib
  ```

### 3. Install Jupyter (Optional)

If you want to run the notebook in VS Code:
```sh
pip install notebook
```

## Usage

1. Place images of known faces in the `Faces/` directory. Each image filename should be the person's name (e.g., `John.jpg`).
2. Open `faceRecognition.ipynb` in Jupyter or VS Code.
3. Run the notebook. The webcam will activate and start recognizing faces.
4. Audio feedback will be played for each detection.

## File Structure

- `faceRecognition.ipynb`: Main notebook for running the face recognition system.
- `Faces/`: Directory containing images of known people.
- `.ipynb_checkpoints/`: Jupyter notebook checkpoints.

## Notes

- Make sure your webcam is connected and accessible.
- The notebook deletes the temporary audio file (`output.mp3`) after playback.
- If you have trouble installing `dlib`, refer to the official
