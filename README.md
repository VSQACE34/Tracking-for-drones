# 🛰️ TelloBoost Tracker: Open-Source Drone Object Tracking Suite

Welcome to **TelloBoost Tracker**, an open-source project designed to explore, test, and evaluate various object tracking algorithms using the **DJI Tello Boost** drone. This project aims to determine which tracking algorithms are best suited for small drones under real-world constraints through rigorous testing, data collection, and community input.

---

## 🚀 Why Object Tracking for Drones?

Object tracking enables drones to autonomously follow or observe targets—whether it's a person, vehicle, or a specific item like a blue mug. This has wide-ranging applications in:

- Aerial cinematography
- Search and rescue
- Surveillance and monitoring
- Hobbyist robotics

However, real-world tracking is challenging due to:

- 🌦️ Varying lighting conditions  
- 🙈 Occlusions or partially visible targets  
- 🎨 Similar-colored backgrounds  
- ⚡ Real-time, low-latency control needs in lightweight drones  

This project aims to **identify which tracking algorithms actually work in such scenarios** on a compact and accessible platform like the Tello Boost.

---

## 🔍 Algorithms Explored

This repository includes implementations and comparisons of the following tracking methods:

### ✅ 1. Color-Based Tracking (Currently Implemented)
Tracks objects based on HSV color filtering (e.g., a deep blue mug), using OpenCV and `djitellopy` for real-time control.

- ✅ Lightweight & fast — perfect for low-resource drones  
- ❌ Sensitive to lighting changes and complex backgrounds  

---

### 🧠 2. Object Detection + Tracking (Coming Soon)
Uses deep learning models such as **YOLOv8** combined with trackers like **Deep SORT** to follow specific classes of objects (cars, people, etc.).

- ✅ Robust to occlusions and scale changes  
- ❌ Requires GPU or edge computing — might exceed Tello’s onboard capabilities  

---

### 🧬 3. Feature-Based Tracking (Planned)
Utilizes methods like ORB, SIFT, or SURF to track textured object features like edges and corners.

- ✅ Great for rich, textured surfaces  
- ❌ Poor performance on smooth or plain-colored objects  

---

### 🔎 4. Template Matching (To Be Evaluated)
Applies OpenCV’s `cv2.matchTemplate()` to detect and track based on a reference image.

- ✅ Simple to implement  
- ❌ Not suitable for scale or rotation variations  

---

## ⚙️ Current Features

- ✅ HSV-based object tracking with real-time Tello Boost feed  
- ✅ Autonomous drone movement in response to object position and size  
- ✅ Command throttling to smooth out movement jitter  
- ✅ Support for future WASD-style manual override  

---


**Dependencies:**
- `opencv-python`
- `numpy`
- `djitellopy`

---

## 📹 Demos & Results

### Color-Based Tracking
[▶️ Watch Tracking Demo (Color Track)](https://github.com/VSQACE34/Tracking-for-drones/blob/main/color%20based%20tracking/tracking_demo(color%20track).mp4)


---

## 🧪 Future Plans

- 🔁 Add support for YOLOv8 + Deep SORT object detection & tracking  
- 🧩 Implement ORB/SIFT-based feature tracking  
- 📊 Benchmark FPS, stability, and accuracy across methods  
- 📖 Publish findings in a final comparative report  

---

## 🤝 Contributions Welcome!

Got a better tracking algorithm to test? Want to improve the PID control?  
Feel free to open an issue or submit a pull request!  
Together we’ll make this the **go-to repo for drone tracking research on Tello.**

---
