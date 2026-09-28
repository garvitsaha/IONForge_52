# IonForge — Smart Fall Detection & Caregiver Monitoring System

## 📌 Project Overview

IonForge is an IoT-based smart fall detection and caregiver monitoring system designed to detect fall events, capture location information, and provide the event details through a connected monitoring dashboard.

The system combines an ESP32-based wearable device, MPU6050 motion sensing, GPS, local emergency alerts, a Node.js backend, database storage, and a React web dashboard.

Each detected fall is represented by a unique Fall Event ID so that the same event can be tracked across the system.

---

## 🎯 Problem Statement

Falls can become serious emergencies when a person is alone or when caregivers are not immediately aware of the incident.

IonForge aims to provide a connected system that can:

- Detect sudden fall-like movement
- Generate a unique fall event
- Capture GPS location
- Provide local emergency alerts
- Send event information to a backend
- Display the event on a caregiver dashboard
- Maintain a history of fall events

---

## ⚙️ System Workflow

Fall Detection
↓
ESP32 Processing
↓
Local Buzzer / Vibration / LED Alert
↓
GPS Location
↓
Wi-Fi
↓
Node.js Backend
↓
Database
↓
React Caregiver Dashboard

---

## 🔧 Hardware Components

- ESP32 DevKit V1
- MPU6050 Accelerometer + Gyroscope
- NEO-6M GPS Module
- OLED Display
- Active Buzzer
- Vibration Motor
- Red LED
- Green LED
- SOS Button
- Rechargeable Battery
- TP4056 Charging Module
- NPN Transistor

---

## 💻 Software Technologies

### Embedded System
- Arduino/C++
- ESP32
- MPU6050
- GPS

### Backend
- Node.js
- Express.js
- JSON/local database
- REST API

### Frontend
- React
- Vite
- Axios
- Web dashboard

### Mapping
- Leaflet
- OpenStreetMap

---

## 🚨 Main Features

- Smart fall detection
- Unique Fall Event ID
- GPS location tracking
- Local emergency alert
- SOS button support
- Device status monitoring
- Caregiver dashboard
- Fall event history
- Backend API
- Hardware-to-software communication
- Wokwi prototype

---

## 🔑 Fall Event

Each fall generates a unique event ID.

Example:

ION-FALL-1790611498631-d313a4

The event can contain:

- Event ID
- Device ID
- Person ID
- Latitude
- Longitude
- GPS availability
- Timestamp
- Alert status
- Caregiver acknowledgement

One fall = One unique event.

---

## 🌐 Backend API

The backend runs on:

http://localhost:5000

### Health Check

GET:

/api/health

### Fall Event

POST:

/api/esp32/fall

The fall event API receives information from the ESP32 system and stores the event for the dashboard.

---

## 🖥️ Frontend Dashboard

The React dashboard runs on:

http://localhost:5173

The dashboard can display:

- Backend connection status
- Device online status
- Person ID
- Device ID
- Fall Event ID
- GPS coordinates
- Location availability
- Fall event information

The prototype also includes a:

**TEST FALL ALERT**

button for demonstrating the complete software workflow without physical hardware.

---

## 🧪 Wokwi Prototype

The ESP32 portion of the project can be tested using Wokwi.

The Wokwi prototype demonstrates the embedded-system logic and sensor workflow.

The final hardware version is intended to integrate the physical components into a wearable/PCB-based device.

---

## 📦 Complete Project Download


Already provided above

Frontend zip is also been provided above 

wowki simulation is also provided above 


---

## ▶️ Running the Backend

```bash
cd IONFORGE_Backend
npm install
node server.js
