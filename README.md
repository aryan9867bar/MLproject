# Facial Emotion Recognition System

A real-time Facial Emotion Recognition system built using Dlib, Keras, OpenCV, and Face Recognition.
The system can identify known individuals and analyze their emotions from live webcam feeds or video files using a deep learning model trained on the FER-2013 dataset.

## 🧠 Overview

This system combines three powerful capabilities into one seamless application:

- 🧍 **Face Detection** — Detects faces in live camera feeds or videos using Dlib’s HOG-based detector.  
- 👁️ **Face Recognition** — Identifies known individuals using preloaded encodings and the `face_recognition` library.  
- 😀 **Emotion Classification** — Classifies real-time emotions such as *Happy*, *Sad*, *Angry*, *Surprise*, and *Neutral* using a CNN model.  

It supports both webcam input and video file analysis, and can be customized with your own emotion model and known faces.


## ✨ Features

### 🎯 Multi-Functional Capabilities

- **Face Detection:** Detects all visible faces in a video stream or image.  
- **Face Recognition:** Identifies known individuals using preloaded encodings.  
- **Emotion Detection:** Classifies emotions such as *Happy*, *Sad*, *Angry*, *Surprise*, and *Neutral*.


## 🧩 Supported Emotions

| Emotion | Description |
|:--------:|:------------|
| 😃 **Happy** | Joyful, pleased, or content |
| 😢 **Sad** | Unhappy or down |
| 😠 **Angry** | Frustrated or annoyed |
| 😮 **Surprise** | Shocked or amazed |
| 😐 **Neutral** | Calm or relaxed |


## 🎨 Visual Indicators

- **Bounding Boxes:** Drawn around detected faces in the video or image.  
- **Color-Coded Labels:** Represent different emotion types for easy visual distinction.  
- **Name + Emotion Overlay:** Displays labels such as *“Aryan is Happy”* directly on the frame.

## ⚙️ System Architecture

| Component | Description |
|:----------:|:------------|
| **Face Detection** | Dlib frontal face detector (HOG) |
| **Face Recognition** | `face_recognition` library with pre-encoded faces |
| **Emotion Classification** | CNN model trained on FER-2013 dataset |
| **Preprocessing** | Custom preprocessing using the `utils` module |
| **Visualization** | Bounding boxes and emotion labels rendered via OpenCV |


## 🚀 How to Run the Project

Follow the steps below to set up and run the **Facial Emotion Recognition** project:

---

### 🧩 1. Install Anaconda

Download and install **Anaconda** from [https://www.anaconda.com/download](https://www.anaconda.com/download)

Once installed, open the **Anaconda Prompt** (or your terminal).

---

### 📦 2. Create & Activate Environment

Create a new environment named `facerec` and activate it:

```bash
conda create -n facerec python=3.10
conda activate facerec


---

### 📚 3. Install Required Libraries

Install the essential Python libraries:

```bash
pip install opencv-python tensorflow keras numpy pandas matplotlib

💡 Add any other dependencies if required.

---

### 📦 4. Run the Project

Once all dependencies are installed, run the project using the following command in your terminal:

```bash
/opt/anaconda3/envs/facerec/bin/python "/Users/apple/Documents/E Drive/FacialEmotion/face-rec-emotion.py"

💡 Tip: You can also open the script in your IDE (like VS Code or Jupyter Notebook) and run it directly.

---

## ✅ 5. Output

### 🎯 Multi-Functional Capabilities

- The program will open your webcam and detect facial emotions in real time.
- Detected emotions such as Happy, Sad, Angry, Surprise, and Neutral will be displayed on the screen with bounding boxes and labels.

---

## 🧠 Technical Details

| Parameter | Description |
|:----------:|:------------|
| **Frameworks** | Keras, Dlib, OpenCV, Face Recognition |
| **Dataset Used** | FER-2013 |
| **Model Type** | CNN (Convolutional Neural Network) |
| **Average Performance** | ~25–30 FPS (on mid-range GPU) |
| **Emotion Window** | Rolling average over 10 frames for stability |
| **Languages** | Python |
| **Libraries** | NumPy, Imutils, OpenCV, Dlib, TensorFlow/Keras |


## ⚡ Troubleshooting

| Problem | Possible Solution |
|:--------|:------------------|
| **ModuleNotFoundError: No module named 'dlib'** | Install **CMake** and **Boost**, then reinstall Dlib. |
| **No face detected** | Improve lighting or ensure you are facing the camera directly. |
| **Model not found** | Ensure `emotion_model.hdf5` exists under the `/models/` directory. |
| **Lag or slow FPS** | Reduce camera resolution or switch to **CPU-only** mode. |
| **face_recognition error** | Verify that all input images are **clear, frontal photos** of faces. |


## 🔮 Future Improvements

In the future, this project can be enhanced by improving model accuracy using larger and more diverse datasets. Real-time performance can be optimized with GPU acceleration and faster frame processing. Additionally, integrating transfer learning and building a web or mobile interface will make the system more powerful and user-friendly.

## 📜 License

This project is licensed under the **MIT License** — you are free to **use**, **modify**, and **distribute** this work with proper attribution.

