# 🚨Accident_detection_system

The system is an intelligent real-time accident detection system that utilizes computer vision and deep learning to recognize vehicle collisions from video uploaded to it and then automatically communicates emergency alerts via Telegram.

---

# 📖 Overview

This project aims to enhance the safety aspects of a road by automatically identifying an accident using traffic or vehicle images. It relies on the YOLOv8 object detection model to detect vehicles in video frames, and calculates possible collisions through IoU (Intersection over Union) calculations.

If an accident is noted:
The accident frame is recorded
Storage in local image database.Storage of the image on the local image database.
An alert via Telegram is sent immediately.

The project is constructed using Flask to create web interface and OpenCV to process video.

---

# ✨ Features

Upload and edit accident videos
Implementing vehicle detection with YOLOv8.- 🚛 YOLOv8 for vehicle detection.
Collisions can be detected based on the IoU thresholding.Collisions can be detected with IoU thresholding.
- 📸 Auto Accident Framing
Integrate Telegram alert system to notify users.Integrate Telegram alert system.
The statistics are processed in real-time with the frame.
- 🌐 Web interface built with simple flask

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Backend Programming |
| Flask | Web Framework |
| OpenCV | Video Processing |
| YOLOv8 | Vehicle Detection |
Object Detection | YOLOv8 | YOLOv3 |
Telegram Bot API is an alert notification system.

---

# 📂 Project Structure

``` id="1mx4fk"
Accident-Detection-System/
│
├── static/
│   └── detected_frames/      # Saved accident frames
│
├── templates/
│   └── index.html            # Frontend page
│
├── uploads/                  # Uploaded videos
├── frames/                   # Extracted frames
│
├── app.py                    # Main Flask application
├── requirements.txt          # Project dependencies
├── README.md                 # Project documentation
└── yolov8n.pt                # YOLOv8 pretrained model
```

---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/Accident-Detection-System.git
```

Click on Project Folder.Click on Project Folder.

```bash id="r97g67"
cd Accident-Detection-System
```

Create Virtual Environment (Optional)

```bash id="7a8b8f"
python -m venv venv
```

## 4️⃣ Activate Virtual Environment

### Windows

```bash id="u4mltx"
venv\Scripts\activate
```

### Linux / Mac

```bash id="2fll5u"
source venv/bin/activate
```

## 5️⃣ Install Dependencies

```bash id="0k2k5f"
pip install -r requirements.txt
```

---

# ▶️ Run the Project

```bash id="ndptx9"
python app.py
```

Open browser and enter:

``` id="scb0s9"
http://127.0.0.1:5000/
```

---

# 🚀 How the System Works

2. The video gets uploaded to the site and becomes visible for all users.3. The uploaded video is displayed for everyone.
3. Using OpenCV, videos are broken into frames.4. OpenCV breaks a video into frames.
3. YOLOv8 detects vehicles in each frame
4. IoU takes the ratio of the area of the vehicles' bounding boxes.
If overlap is greater than the threshold:
   - Accident is detected
   - Frame is saved
   - Telegram alert is triggered

---

# 🔔 Telegram Alert Integration

When an accident is detected, the system notifies the users by sending a message via Telegram.

You need:
- Telegram Bot Token
- Chat ID

Make sure they are set up before the project is run within the Python file.

---

# 📌 Notes

- Resumes YOLOv8 nano model (yolov8n.pt) for pretraining.
- Processes every 5th frame to improve performance.
- IoU threshold reduces false positive
- For Education and Research

---

# 📸 Future Improvements

- Live CCTV support for streams.
- GPS location integration
- Emergency service automation
- Better accident learning and information exchange performance
- Cloud deployment support

---

# 🤝 Contributors

- Abhishek Mishra and Team

---

# 📜 License

This project is under the MIT License.

---

# ⭐ Support

If you enjoy this project, maybe you can give it a ⭐ on GitHub.
