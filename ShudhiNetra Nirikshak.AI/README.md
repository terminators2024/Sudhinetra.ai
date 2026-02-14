<div align="center">

  <img src="assets/team/shuddhinetra_logo.jpeg" alt="ShuddhiNetra Logo" width="200" height="auto" />
  <br/>

  # 🏆 ShuddhiNetra Nirikshak
  ### AI-Driven Cleanliness Monitoring System
  
  **Team TERMINATORS | Smart India Hackathon 2024**

  [![SIH 2024](https://img.shields.io/badge/SIH-2024-orange?style=for-the-badge&logo=india)](https://sih.gov.in)
  [![Team](https://img.shields.io/badge/Team-TERMINATORS-blue?style=for-the-badge&logo=github)](https://github.com/Atoleanantha)
  [![Problem Statement](https://img.shields.io/badge/Problem_Statement-SIH1751-green?style=for-the-badge)](#)
  [![Status](https://img.shields.io/badge/Status-Prototype-success?style=for-the-badge)](#)
  [![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

  <p>
    <a href="https://shuddinetrasih1751.icipamrutvahini.in/"><b>🌐 Live Prototype</b></a> •
    <a href="https://youtu.be/AvnI_TFHcHY?si=vH3_ij6yC5JE1xNs"><b>📺 Video Demo</b></a> •
    <a href="assets/docs/presentation.pptx"><b>📊 Pitch Deck</b></a> •
    <a href="https://github.com/Atoleanantha/SIH_Shuddhi_Netra.git"><b>💻 Source Code</b></a>
  </p>

</div>

---

## 📖 Table of Contents
- [🚀 Project Overview](#-project-overview)
- [✨ Key Features](#-key-features)
- [🛠️ Technology Stack](#-technology-stack)
- [🏗️ System Architecture](#-system-architecture)
- [📂 Project Structure](#-project-structure)
- [📑 Documents & Reports](#-documents--reports)
- [🏅 Certificates & Achievements](#-certificates--achievements)
- [👥 Team Terminators](#-team-terminators)
- [⚙️ Installation & Setup](#-installation--setup)

---

## 🚀 Project Overview

**ShuddhiNetra Nirikshak** is a cutting-edge **AI-powered surveillance system** engineered for the **Department of Posts** to revolutionize Swachhta (cleanliness) and LiFE (Lifestyle for Environment) monitoring.

Leveraging existing CCTV infrastructure, our system deploys **Computer Vision (YOLOv9)** to autonomously detect garbage, segregation violations, and environmental anomalies in real-time. It empowering Divisional Officers with a **centralized dashboard** to monitor compliance, trigger instant alerts, and generate data-driven insights for a cleaner, greener India.

> **Problem Statement Title:** Dashboard for Swachhta and LiFE  
> **Theme:** Clean & Green Technology

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| **🤖 AI-Powered Detection** | Real-time identification of waste (plastic, paper, metal) using **YOLOv9** with strided inference. |
| **🔍 Tiny Object Recon** | Optimized algorithms to detect small litter items often missed by standard surveillance models. |
| **📄 Smart Doc Verification** | Integration of **ESRGAN** (Super Resolution) to clarify text/digits in low-resolution video feeds. |
| **📊 Central Command** | A unified dashboard for Divisional Officers to monitor multiple Post Offices simultaneously. |
| **📍 Geotagged Alerts** | Instant visual alerts with precise timestamps and location data for rapid response. |
| **📈 Waste Analytics** | Comprehensive reports with "hotspot" analysis using **KNN & Chameleon Clustering**. |
| **� Route Optimization** | AI-driven route planning using **Google Maps API** & **OR-Tools** for efficient waste collection. |

---

## 🛠️ Technology Stack

<div align="center">

| **Frontend** | **Backend** | **AI / ML** | **Database & Cloud** |
| :---: | :---: | :---: | :---: |
| ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) | ![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white) | ![YOLOv9](https://img.shields.io/badge/YOLOv9-00FFFF?style=for-the-badge&logo=python&logoColor=white) | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white) |
| ![MUI](https://img.shields.io/badge/MUI-007FFF?style=for-the-badge&logo=mui&logoColor=white) | ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) | ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white) | ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black) |
| **Folium Maps** | **DRF** | **PyTorch** | **Google Maps API** |

</div>

---

## 🏗️ System Architecture

```mermaid
graph TD
    subgraph Input
    A[CCTV Camera Network] -->|Video Stream| B[Preprocessing Node]
    end
    
    subgraph "AI Inference Engine"
    B -->|Frames| C{Analysis}
    C -->|Object Detection| D[YOLOv9 Model]
    C -->|Super Resolution| E[ESRGAN Model]
    end
    
    subgraph "Backend Processing"
    D & E -->|Anomalies| F[Django API]
    F -->|Store Data| G[(Database)]
    F -->|Trigger| H[Notification Service]
    end
    
    subgraph Output
    H -->|Alert| I[Cleaning Staff App]
    F -->|Analytics| J[Admin Dashboard]
    J -->|Visualize| K[3D Maps & Reports]
    end
```

---

## 📂 Project Structure

```bash
ShudhiNetra-Nirikshak/
├── backend/                  # Django Backend Logic
│   ├── post_office/          # Office Management
│   ├── waste_management/     # Waste Analytics APIs
│   └── users/                # Auth & Role Management
│
├── frontend/                 # React User Interface
│   ├── src/components/       # UI Components
│   └── src/services/         # API Integrations
│
├── assets/                   # Project Resources
│   ├── team/                 # Team Photos & Logos
│   ├── docs/                 # Reports & Presentations
│   └── certificates/         # Achievements
│
└── README.md                 # Documentation (You are here!)
```

---

## 📑 Documents & Reports

| Document | Description | View / Download |
| :--- | :--- | :---: |
| **📊 Final Presentation** | Complete project pitch deck highlighting solution & impact. | [Download PPT](assets/docs/project_presentation.jpeg) |
| **� Project Report** | Detailed technical documentation and implementation guide. | [View PDF](assets/docs/project_report.pdf) |
| **📉 Survey Report** | Analysis of survey findings and site visit data. | [View PDF](assets/docs/survey_and_visit_report.pdf) |

---

## 🏅 Certificates & Achievements

<div align="center">
  <table>
    <tr>
      <td align="center">
        <img src="assets/certificates/certificate_1.jpeg" width="400" alt="Certificate 1"><br>
        <b>🥇 Achievement Certificate</b>
      </td>
      <td align="center">
        <img src="assets/certificates/certificate_2.jpeg" width="400" alt="Certificate 2"><br>
        <b>🥈 Participation Certificate</b>
      </td>
    </tr>
  </table>
</div>

---

## 👥 Team Terminators

<div align="center">
  <img src="assets/team/team_photo.jpeg" width="800" alt="Team Terminators Group Photo" style="border-radius: 10px; box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);">
  <br/><br/>
  
  ### 🏫 Amrutvahini College of Engineering, Sangamner
  
  <table>
    <tr>
      <td align="center">
        <img src="assets/members/Narendra.jpg" width="100" style="border-radius: 50%;"><br>
        <b>Narendra Wakhare</b><br>
        <i>Team Lead</i>
      </td>
      <td align="center">
        <img src="assets/members/Ananta.jpg" width="100" style="border-radius: 50%;"><br>
        <b>Ananta Atole</b><br>
        <i>Full Stack Developer</i>
      </td>
       <td align="center">
        <img src="assets/members/Tushar.jpg" width="100" style="border-radius: 50%;"><br>
        <b>Tushar Bendre</b><br>
        <i>Backend Developer</i>
      </td>
    </tr>
     <tr>
      <td align="center">
        <img src="assets/members/Hrishikesh.jpg" width="100" style="border-radius: 50%;"><br>
        <b>Hrishikesh Gurap</b><br>
        <i>Frontend Developer</i>
      </td>
      <td align="center">
        <img src="assets/members/Yash.jpg" width="100" style="border-radius: 50%;"><br>
        <b>Yash Gorde</b><br>
        <i>Data Engineer</i>
      </td>
       <td align="center">
        <img src="assets/members/Mayuri.jpg" width="100" style="border-radius: 50%;"><br>
        <b>Mayuri</b><br>
        <i>R&D and Documentation</i>
      </td>
    </tr>
  </table>
</div>

---

## ⚙️ Installation & Setup

<details>
<summary><b>Click to expand Installation Guide</b></summary>

### Prerequisites
- Node.js (v16+)
- Python (v3.9+)
- PostgreSQL (optional)

### 1. Clone the Repository
```bash
git clone https://github.com/Atoleanantha/SIH_Shuddhi_Netra.git
cd SIH_Shuddhi_Netra
```

### 2. Backend Setup
```bash
cd backend
python -m venv env
# Activate: .\env\Scripts\activate (Win) or source env/bin/activate (Mac/Linux)
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### 3. Frontend Setup
```bash
cd frontend
npm install
npm start
```
</details>

---

> *"Swachhta is not just a mission, it is a lifestyle."* 🌱
