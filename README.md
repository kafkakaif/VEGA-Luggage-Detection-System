<h1 align="center"> VEGA – Luggage Detection System</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Framework-YOLOv5-orange?logo=github" alt="YOLOv5">
  <img src="https://img.shields.io/badge/WebApp-Streamlit-red?logo=streamlit" alt="Streamlit">
  <img src="https://img.shields.io/badge/Status-Active-success?logo=github" alt="Status">
</p>

<p align="center">
  <i>“Empowering safer travel through intelligent vision.”</i>
</p>

---

## Overview

**VEGA** is an **AI-powered luggage scanning and detection system** built using **YOLOv5** and **computer vision**.  
It automatically detects suspicious or prohibited items inside luggage using deep learning, transforming traditional baggage screening into a **smart, real-time, and efficient** process.

---

## Features

- ⚡ **Real-Time Detection** — Instant and accurate luggage item detection using YOLOv5  
- 🧠 **AI-Powered Insights** — Trained on a custom dataset for robust performance  
- 🌐 **Interactive Web Interface** — Upload luggage images directly from the browser  
- 📊 **Automated Logs & Reports** — Save detection results with confidence scores  
- 🔒 **Security-Focused Design** — Enhances airport and transport screening systems  

---

## Tech Stack

| Category | Technologies Used |
|-----------|------------------|
| 💻 **Language** | Python |
| 🧠 **AI Model** | YOLOv5 |
| 🌐 **Frontend / Web** | Streamlit |
| 🧩 **Libraries** | OpenCV, NumPy, Pandas |
| 🧱 **Backend Framework** | Flask |
| 🗂️ **Version Control** | Git & GitHub |

---

## Project Structure

VEGA-Luggage-Detection-System/
│
├── yolov5/ # YOLOv5 model files
├── data/ # Training and test data
├── runs/ # Detection results
├── app.py # Streamlit web app
├── detect.py # YOLOv5 detection script
├── requirements.txt # Dependencies
├── README.md # Documentation
└── utils/ # Helper scripts


---

## Installation

```bash
# 1️⃣ Clone the repository
git clone https://github.com/kafkakaif/VEGA-Luggage-Detection-System.git
cd VEGA-Luggage-Detection-System

# 2️⃣ Install dependencies
pip install -r requirements.txt

# 3️⃣ Run the Streamlit app
streamlit run app.py


---

##  Installation

```bash
# 1️⃣ Clone the repository
git clone https://github.com/kafkakaif/VEGA-Luggage-Detection-System.git
cd VEGA-Luggage-Detection-System

# 2️⃣ Install dependencies
pip install -r requirements.txt

 Dataset & Model Training
 Dataset

The dataset contains labeled images of luggage and prohibited objects (e.g., knives, bottles, tools, electronics, etc.) for model training.
You can use:

Custom collected dataset

Or public datasets such as Security Baggage X-ray Dataset (SIXray) or GDXray

Structure Example:

datasets/
│
├── images/
│   ├── train/
│   └── val/
│
└── labels/
    ├── train/
    └── val/

Training YOLOv5

To train your own model:

# Navigate to YOLOv5 directory
cd yolov5

# Train the model
python train.py --img 640 --batch 16 --epochs 100 --data data.yaml --weights yolov5s.pt --name vega-luggage


After training, your weights will be saved at:

runs/train/vega-luggage/weights/best.pt


Use them for detection by placing best.pt in your project root and updating detect.py:

python detect.py --weights best.pt --source test_images/

Project Goal

To develop a smart luggage inspection assistant that helps security personnel automatically detect prohibited or suspicious items efficiently — reducing human effort and improving screening accuracy.

# 3️⃣ Run the Streamlit app
streamlit run app.py

Project Goal

To develop a smart luggage inspection assistant that helps security personnel automatically detect prohibited or suspicious items efficiently — reducing human effort and improving screening accuracy.

Vision
“Making security smarter, faster, and safer with AI.”
