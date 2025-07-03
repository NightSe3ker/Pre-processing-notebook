# 🚗 Motion Detection & Vehicle Segmentation using Image Pre-processing

This project demonstrates a basic yet powerful **video frame pre-processing pipeline** using OpenCV. It focuses on detecting **motion** (e.g., moving vehicles) in video footage by analyzing the differences between **two consecutive frames**.

This notebook showcases common image processing techniques including blurring, thresholding, morphological operations, and contour detection — all essential steps in building real-world computer vision systems for **vehicle detection**, **object tracking**, and **video surveillance**.

---

## 🎯 Objective

To identify and segment moving vehicles from a video stream by applying frame differencing and a series of image pre-processing steps that help isolate motion from static backgrounds.

---

## 📌 What This Code Does

### 🖼️ 1. Frame Capture
- Captures **two consecutive frames** from a video stream or video file.
- Motion is determined based on **pixel value differences** between these frames.

### 🌀 2. Frame Differencing
- Subtracts pixel values of the two frames to highlight **regions of change (motion)**.
- Works on the principle that moving objects result in a noticeable pixel difference between frames.

### 🧼 3. Gaussian Blur
- Applies **Gaussian smoothing** to reduce noise and soft edges.
- This helps in preventing false detections in later steps.

### 🎚️ 4. Thresholding
- Converts the blurred image into a **binary format** (black & white).
- Pixels below a threshold are set to black, others to white, emphasizing moving objects.

### 🧱 5. Morphological Operations
- **Dilation**: Expands white regions to connect fragmented parts of an object.
- **Erosion**: Shrinks white regions to eliminate small noise.
- These operations help in **cleaning up** the binary image.

### 🔍 6. Contour Detection
- Finds **boundaries of distinct regions** (contours) in the thresholded image.
- These contours correspond to **moving objects**, such as vehicles.

### 🔄 7. Convex Hulls
- Calculates the **convex hulls** of contours for more accurate and simplified object shapes.
- This step improves shape approximation and helps in identifying vehicles more clearly.

---

## 🛠️ Tools and Technologies Used

| Tool / Library     | Purpose                                               |
|--------------------|-------------------------------------------------------|
| **Python**         | Programming language                                  |
| **OpenCV** (`cv2`) | Image processing, video frame handling, contour ops  |
| **NumPy**          | Numerical computations on frame data                  |
| **Matplotlib**     | (Optional) For displaying images and visual debugging |

---

## 🚀 Applications

This pre-processing pipeline can be extended to:
- 🚦 Traffic Monitoring Systems
- 🛣️ Vehicle Counting and Speed Estimation
- 🔐 Surveillance Cameras for Motion Detection
- 🤖 Smart City & AI-powered Traffic Analysis

---

## 📋 Requirements

Install the following Python libraries:

```bash
pip install opencv-python numpy matplotlib

