# 🏆 ShuddhiNetra Nirikshak - AI-Driven Cleanliness Monitoring System
### Team TERMINATORS | Smart India Hackathon 2024

[![SIH 2024](https://img.shields.io/badge/SIH-2024-orange)](https://sih.gov.in)
[![Team](https://img.shields.io/badge/Team-TERMINATORS-blue)](#)
[![Problem Statement](https://img.shields.io/badge/Problem_Statement-SIH1751-green)](#)

**Problem Statement Title:** Dashboard for Swachhta and LiFE (Lifestyle for Environment)  
**Theme:** Clean & Green Technology  
**Result:** [Add Status, e.g., Finalist/Winner]

---

## 🚀 Project Overview

**ShuddhiNetra Nirikshak** is an AI-powered surveillance and monitoring system designed for the **Department of Posts** to automate the monitoring of cleanliness (Swachhta) and environmental practices (LiFE). 

Using existing CCTV infrastructure, the system leverages **Computer Vision (YOLOv9)** to detect garbage, segregation non-compliance, and other anomalies in real-time. It provides a centralized dashboard for divisional officers to monitor multiple post offices, trigger alerts, and generate actionable analytics for a cleaner and greener environment.

### 🔗 Key Links
- **📺 Video Demo:** [Watch on YouTube](https://youtu.be/AvnI_TFHcHY?si=vH3_ij6yC5JE1xNs)
- **🌐 Live Website:** [ShuddhiNetra Portal](https://shuddinetrasih1751.icipamrutvahini.in/)
- **💻 GitHub Repo:** [View Source](https://github.com/Atoleanantha/SIH_Shuddhi_Netra.git)

---

## ✨ Key Features

### 🤖 AI-Powered Monitoring
- **Real-time Garbage Detection:** Uses **YOLOv9** with strided inference to detect waste objects (plastic, paper, metal, etc.) from CCTV feeds.
- **Tiny Object Detection:** Optimized for identifying small waste items often missed by standard models.
- **Document Verification:** Integrates **ESRGAN** (Super Resolution) to enhance legibility of text/digits in low-res footage.

### 📊 Interactive Dashboard
- **Centralized View:** Single pane of glass for Divisional Officers to monitor all subordinate Post Offices.
- **Geotagged Alerts:** Real-time visual alerts with timestamps and location data when cleanliness standards are violated.
- **Waste Analytics:** Detailed reports on waste generation, segregation compliance, and "hotspot" analysis using **KNN & Chameleon Clustering**.

### 📱 Smart Notifications
- **Instant Alerts:** Cloud-based notifications (Firebase) sent to cleaning staff and administrators immediately upon detection.
- **Route Optimization:** Uses **Google Maps API** and **OR-Tools** to suggest the most efficient waste collection routes for staff.

---

## 🛠️ Technology Stack

| Component | Technologies |
|-----------|--------------|
| **Frontend** | React.js, Material UI, Folium (Maps), Recharts |
| **Backend** | Django Rest Framework (DRF), Python |
| **AI / ML** | YOLOv9, OpenCV, PyTorch, TensorFlow, ESRGAN |
| **Database** | PostgreSQL / SQLite |
| **Integrations** | Firebase (FCM), Google Maps API, O/R Tools |
| **Deployment** | Vercel (Frontend), Render/AWS (Backend) |

---

## 🏗️ System Architecture

```mermaid
graph TD
    A[CCTV Camera Network] -->|Video Stream| B[Preprocessing Node]
    B -->|Frames| C{AI Inference Engine}
    C -->|Detect Garbage| D[YOLOv9 Model]
    C -->|Enhance Text| E[ESRGAN Model]
    D & E -->|Anomalies Detected| F[ backend API (Django)]
    F -->|Store Data| G[(Database)]
    F -->|Push Notification| H[Firebase Cloud Messaging]
    H -->|Alert| I[Cleaning Staff App]
    F -->|Analytics API| J[Admin Dashboard (React)]
    J -->|Visualize| K[3D Maps & Reports]
```

---

## 📂 Project Structure

```bash
ShudhiNetra-Nirikshak/
├── backend/                  # Django Backend
│   ├── backend/              # Project Settings & Config
│   ├── post_office/          # App: Manage PO & Divisions
│   ├── users/                # App: User Roles (Divisional/Sub-divisional)
│   ├── waste_management/     # App: E-waste, Paper waste APIs
│   ├── manage.py             # Django Entry Point
│   └── requirements.txt      # Python Dependencies
│
├── frontend/                 # React Frontend
│   ├── public/               # Static Assets
│   ├── src/
│   │   ├── components/       # Reusable UI Components
│   │   ├── services/         # API Service Calls (Axios)
│   │   ├── App.js            # Main Application Component
│   │   └── index.js          # React Entry Point
│   └── package.json          # Node Dependencies
│
└── README.md                 # Project Documentation
```

---

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v16+)
- Python (v3.9+)
- PostgreSQL (optional, can use SQLite for dev)

### 1. Clone the Repository
```bash
git clone https://github.com/Atoleanantha/SIH_Shuddhi_Netra.git
cd SIH_Shuddhi_Netra
```

### 2. Backend Setup
Navigate to the backend directory and set up the Python environment.

```bash
cd backend
# Create virtual environment
python -m venv env
# Activate environment (Windows)
.\env\Scripts\activate
# Activate environment (Mac/Linux)
source env/bin/activate

# Install dependencies
pip install -r requirements.txt
# Note: If requirements.txt is minimal, ensure django, djangorestframework, django-cors-headers are installed.

# Run Migrations
python manage.py migrate

# Start Server
python manage.py runserver
```
The backend API will run at `http://localhost:8000`.

### 3. Frontend Setup
Open a new terminal and navigate to the frontend directory.

```bash
cd frontend
# Install dependencies
npm install

# Start React App
npm start
```
The application will open at `http://localhost:3000`.

---

## 📸 Screenshots & Usage

| **Dashboard View** | **Waste Analytics** |
|:---:|:---:|
| ![Dashboard](https://via.placeholder.com/400x200?text=Dashboard+Preview) | ![Analytics](https://via.placeholder.com/400x200?text=Analytics+Graph) |
| *Real-time monitoring of Post Office ambiance* | *Weekly waste generation reports* |

---

## 👥 Team Terminators
- **Problem Statement:** SIH1751
- **College:** Amrutvahini College of Engineering, Sangamner

---

> *"Swachhta is not just a mission, it is a lifestyle."* 🌱
