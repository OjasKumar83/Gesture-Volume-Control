# 🎛️ Gesture-Based Volume Control using Python

A computer vision-based project that allows you to control your **system volume using hand gestures** — just by using your **webcam**. This project uses **OpenCV**, **MediaPipe**, and **PyCaw** to detect the distance between your **thumb and index finger**, and adjusts the system volume accordingly.

---

## 📸 Demo

https://github.com/user-attachments/assets/6d35bf0a-37c5-4509-8a2f-2c3d22223db5

---

## 📌 Features

- 🖐️ Real-time hand tracking
- 🔊 Volume controlled by distance between thumb and index finger
- 🎨 On-screen visuals for feedback (volume bar, % level, finger tips)
- ✅ Close app via ❌ button or press **`q`**
- 🪶 Lightweight and easy to run

---

## 🧠 How It Works

1. **OpenCV** captures real-time webcam frames.
2. **MediaPipe** detects your hand and landmarks.
3. Distance between **thumb tip (ID 4)** and **index finger tip (ID 8)** is calculated using `math.hypot()`.
4. **NumPy** interpolates this distance into a volume percentage (0–100%).
5. **PyCaw** sets the actual system volume using Windows audio APIs.
6. Visual feedback is displayed in the OpenCV window.

---

## ⚙️ Prerequisites

Make sure you are using **Python 3.6 or higher** and are on **Windows OS**.

Install dependencies using:

```bash
pip install opencv-python mediapipe numpy pycaw comtypes
```
> ✅ **Note**: This project works **only on Windows** due to the use of the `pycaw` library,
> which depends on the Windows Core Audio APIs.

---

## ▶️ How to Run

1. Clone this repo or download the `gesture_volume_control.py` file.
2. Run the script using:

```bash
python newMain.py
```

3. Show your hand in front of the webcam.

4. Move thumb and index finger:

  👉 Closer: Decrease volume

  👉 Farther: Increase volume

5. Exit by pressing q or clicking the ❌ window close button.

## 🗂️ File Structure

    gesture_volume_control/
    ├── newMain.py                  # Main application
    ├── demo.gif                    # (Optional) Visual demo
    └── README.md                   # You're reading it now
    
## 🧰 Libraries Used

| Library         | Use Case                                |
| --------------- | --------------------------------------- |
| `opencv-python` | Webcam input, drawing, display UI       |
| `mediapipe`     | Hand landmark detection                 |
| `math`          | Calculating distance between fingers    |
| `numpy`         | Interpolating finger distance to volume |
| `pycaw`         | Changing system volume on Windows       |
| `comtypes`      | Required for `pycaw` COM interface      |

---

## 📚 References

- 📘 [MediaPipe Hands Documentation](https://google.github.io/mediapipe/solutions/hands)
- 📘 [PyCaw GitHub Repository](https://github.com/AndreMiras/pycaw)
- 📘 [OpenCV Python Documentation](https://docs.opencv.org/master/)
- 📘 [NumPy Documentation](https://numpy.org/doc/)
- 📘 [comtypes Library on PyPI](https://pypi.org/project/comtypes/)
- 📘 [math.hypot() — Python Docs](https://docs.python.org/3/library/math.html#math.hypot)

---

## 🚀 Future Improvements

- 🤖 Add support for multi-gesture recognition (e.g., mute, skip, pause)
- 💻 Cross-platform compatibility (support for macOS and Linux using alternative audio libraries)
- 🎨 Enhanced user interface with animated feedback or sound alerts
- 📷 Add calibration step to improve accuracy across hand sizes and lighting conditions

---

## 🙋‍♂️ Author

Developed by **Ojas Kumar**  
📫 Connect with me:  
- [GitHub](https://github.com/OjasKumar83)  
- [LinkedIn](https://www.linkedin.com/in/ojas-kumar-10347a252/)  

> Feel free to fork, improve, or open issues in the repo. Contributions are welcome!


    



