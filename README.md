# ♻️ NEOBIN – Smart Waste Management System

## 📘 Overview
**NEOBIN** is an **AI-powered**, **IoT-enabled** smart waste management system designed to automate waste monitoring, classification, and reporting.  
The system integrates **ultrasonic**, **weight**, and **odor sensors**, along with a **camera module** for image-based waste classification.  
Built using **Raspberry Pi 4**, **PyTorch**, **MongoDB Atlas**, and a **React Native mobile app**, NEOBIN enables **real-time tracking, data-driven insights**, and contributes toward **cleaner, smarter, and sustainable cities**.

---

## 🌍 Problem Statement
Urban waste management is a growing challenge due to:
- Overflowing trash bins and poor segregation  
- Lack of real-time monitoring  
- Inefficient waste collection and route planning  

These issues lead to environmental pollution, higher operational costs, and public health risks.  
**NEOBIN** provides a smart, automated, and scalable solution that minimizes manual intervention and optimizes waste collection processes.

---

## 🎯 Objectives
- ✅ Automatically segregate waste using AI.  
- ✅ Provide real-time monitoring of bin status.  
- ✅ Reduce manual effort and operational costs.  
- ✅ Deliver actionable insights to municipal authorities and citizens.  
- ✅ Promote sustainability through efficient waste management.

---

## 🧩 Components Used

| Component | Description |
|------------|-------------|
| **Raspberry Pi 4** | Acts as the main processing unit integrating sensors and handling data communication. |
| **JSN-SR04T Ultrasonic Sensor** | Measures the fill level of the waste bin. |
| **MQ135 Sensor** | Detects odor and gas concentration levels. |
| **HX711 + Load Cell** | Measures the weight of the waste inside the bin. |
| **Camera Module** | Captures images of waste for AI-based classification. |
| **MongoDB Atlas** | Cloud storage for sensor and image data. |
| **React Native** | Used to build the mobile app for real-time data visualization. |
| **PyTorch** | Deep learning framework for waste classification. |
| **Vercel** | Used for backend deployment and data synchronization. |

---

## ⚙️ Methodology

1. **Sensing Waste Data**  
   Ultrasonic, weight, and odor sensors continuously monitor bin status.

2. **Image Capture & Classification**  
   The camera captures waste images; a **PyTorch-trained deep learning model** classifies the waste as **recyclable** or **non-recyclable**.

3. **Data Processing & Cloud Storage**  
   Raspberry Pi processes sensor and image data, uploading results to **MongoDB Atlas**.

4. **Mobile App Visualization**  
   A **React Native app** provides real-time status, including bin fill levels, odors, and alerts, accessible to both users and authorities.

---

## 🧠 System Architecture

```mermaid
flowchart TD
    A[Waste Bin] --> B[Ultrasonic Sensor]
    A --> C[Weight Sensor]
    A --> D[Odour Sensor]
    A --> E[Camera Module]
    B & C & D & E --> F[Raspberry Pi 4]
    F --> G[AI Model - PyTorch]
    F --> H[MongoDB Atlas - Cloud Storage]
    H --> I[React Native Mobile App]
    I --> J[Users & Municipal Authorities]
