[README.md](https://github.com/user-attachments/files/27798173/README.md)
# Scuba Cat Project

This repository contains the source code for the **Scuba Cat** project, whose objective is to display an animated video/GIF through hand gesture recognition using computer vision.

## IMPORTANT NOTE ABOUT THE PYTHON VERSION

The project MUST be executed using Python 3.10.x, as there are incompatibilities and exceptions in critical libraries (such as MediaPipe) when using a different version (3.11+ or 3.9-). The `main` branch has only been validated for this Python version.

## SYSTEM REQUIREMENTS

- Language: Python 3.10 (Mandatory)
- Libraries: OpenCV, MediaPipe, NumPy
- Hardware: Webcam and the `gato.mp4` video file in the root directory.

## INSTALLATION AND SETUP (BASH)

Follow these steps to prepare your execution environment:

### 1. Clone the repository

If you have not cloned the repository yet, you can do so with the following command:

```bash
git clone //github.com/nikocharlifan-hub/Scubacat.git
cd Scubacat
```

### 2. Create and activate a virtual environment

It is highly recommended to use a virtual environment to avoid conflicts with other Python libraries:

```bash
python -m venv .venv

# On Windows:
.venv\Scripts\activate

# On macOS/Linux:
source .venv/bin/activate
```

### 3. Install the dependencies

Make sure `pip` is updated, then install the required libraries:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## RUNNING THE PROJECT

Once the environment is configured and the dependencies are installed, you can run the project.

### 1. Make sure your webcam is connected and that the `gato.mp4` video file is in the same folder as the script.

### 2. Run the main script

```bash
python scubacat_final.py
```

This will start the detection system, which should begin detecting hand gestures to control video playback.

## VIDEO FILE VERIFICATION

Make sure that the video file named `gato.mp4` is present in the same directory as the script `scubacat_final.py`. If the file is missing, the video will not load.

## GESTURE CONTROL LOGIC

The system monitors 21 key hand points to execute the following actions:

- FIST GESTURE: When the fingers contract toward the base of the palm, automatic video playback starts.
- OPEN PALM GESTURE: When the fingers are extended, the system stops the capture and closes the video window.
- ESC KEY: Ends the main camera capture and closes the program.

## TROUBLESHOOTING GUIDE

If you encounter problems during execution, here are some common solutions:

### PATH ERROR (FileNotFound)

Make sure the video file is named exactly `gato.mp4` and is located in the same folder as the `.py` file.

### THE CAMERA DOES NOT TURN ON

Check that no other application (such as Teams, Zoom, Discord, etc.) is using the webcam in the background.

### ATTRIBUTE ERROR (AttributeError)

If you see an error related to `mediapipe.solutions`, make sure there is no file named `mediapipe.py` in your local folder, as this can interfere with Python imports.

### 'PIP' COMMAND ERROR

If your terminal does not recognize the `pip` command, make sure you are using the correct virtual environment. If it is still not recognized, try the following command:

```bash
python -m pip install --upgrade pip
```

### The video does not play

- Verify that the `gato.mp4` file is in the correct directory and that there are no path errors.
- Also make sure the video format is compatible with OpenCV.

### Problems with gesture detection

- Make sure the camera has good lighting.
- Adjust the position of your hands in front of the camera to ensure they are visible.
- If the “fist” gesture does not start the video, make sure the finger points are close enough to the base of the palm.

