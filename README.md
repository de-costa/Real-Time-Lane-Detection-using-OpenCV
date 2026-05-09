# 🚗 Real-Time Lane Detection using OpenCV

## 📌 Project Overview
This project demonstrates a simple real-time lane/road edge detection system using **Python** and **OpenCV**. The system processes a road driving video, applies image processing techniques, detects lane boundaries/road edges, and estimates the relative distance between the detected lane and the center of the frame.

The project is implemented in a Jupyter Notebook and is designed for learning purposes in the fields of:

- Computer Vision
- Image Processing
- OpenCV Applications

---

## ✨ Features

- 📹 Reads and processes a road driving video
- 🎨 Converts frames into grayscale for easier processing
- 🔍 Applies Sobel edge detection using convolution filtering
- ⚡ Thresholding for highlighting lane edges
- 📦 Contour detection for identifying road lane boundaries
- 📏 Calculates the distance between detected lane and frame center
- 🖼️ Displays processed frames in real time
- 🧠 Demonstrates basic lane tracking concepts used in self-driving systems

---

## 🛠️ Technologies Used

- **Python**
- **OpenCV (cv2)**
- **NumPy**
- **Jupyter Notebook**

---

## 📂 Project Structure

```bash
├── laneDetect.ipynb        # Main Jupyter Notebook
├── road_drive.avi        # Input driving video
└── README.md             # Project documentation
```

---

## ⚙️ How the Project Works

### 1️⃣ Video Capture

```python
source = cv2.VideoCapture("road_drive.avi")
```

### 2️⃣ Grayscale Conversion

```python
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
```

### 3️⃣ Edge Detection using Sobel Kernel

```python
kernel = np.array([
    [-1, 0, 1],
    [-2, 0, 2],
    [-1, 0, 1]
])

conv = cv2.filter2D(gray, -1, kernel)
```

### 4️⃣ Thresholding

```python
ret, thresh = cv2.threshold(conv, 120, 255, 0)
```

### 5️⃣ Contour Detection

```python
contours, hierarchy = cv2.findContours(
    thresh,
    cv2.RETR_TREE,
    cv2.CHAIN_APPROX_SIMPLE
)
```

### 6️⃣ Distance Calculation

```python
distance = frameCx - cx
```

---

## ▶️ Installation & Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

### Step 2: Navigate to the Project Folder

```bash
cd your-repository-name
```

### Step 3: Install Required Libraries

```bash
pip install opencv-python numpy jupyter
```

### Step 4: Run the Notebook

```bash
jupyter notebook
```

Open `laneDetect.ipynb` and run all cells.

---

## 📸 Output

The system displays:

- Original video feed
- Detected lane contours
- Frame center line
- Distance measurement from detected lane

---

## 📖 Learning Outcomes

Through this project, you can understand:

- Basics of computer vision
- Image preprocessing techniques
- Convolution filtering
- Edge detection concepts
- Contour detection in OpenCV
- Real-time video processing
- Fundamental ideas behind autonomous driving systems

---

## 🚀 Future Improvements

Possible improvements for this project include:

- Using Hough Transform for accurate lane detection
- Implementing curved lane tracking
- Real-time webcam integration
- Deep learning-based lane detection
- Steering angle prediction
- Obstacle detection integration
- Performance optimization for real-time systems

---


## 📜 License

This project is open-source and available under the MIT License.

---

## 👨‍💻 Author

Developed by SAUMYA DE COSTA

