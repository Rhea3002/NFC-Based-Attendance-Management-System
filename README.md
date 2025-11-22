# NFC-Based-Attendance-Management-System

The **NFC-Based Attendance Management System** is a smart, automated solution built using **ESP32**, **PN532 NFC module**, and **Google Apps Script** to simplify and digitize attendance tracking. Users simply tap their NFC ID cards, and the system instantly verifies credentials, updates attendance in Google Sheets, and provides real-time feedback on an LCD display.

---

## 🚀 Overview

Designed as an end-to-end embedded + cloud-integrated project, the system replaces manual roll calls with fast, accurate, and reliable NFC-based verification. It supports two operational modes—**Registration** and **Attendance Marking**—and ensures clean data logging through cloud synchronization.

All supporting documentation, flowcharts, and code explanations are included in the project report.

---

## 📱 Core Features

### **NFC-Based Attendance**
- Tap an NFC-enabled card to instantly log attendance.
- Validates user ID, checks duplicates for the day, and stores the entry in Google Sheets.
- LCD shows success, error, or already-marked messages.

### **Registration Mode**
- Add new users by tapping their NFC card.
- Prevents duplicate registration by checking the UID in the database.

### **Google Sheets Integration**
- Attendance is uploaded to Google Sheets in real time.
- Automatically creates new date columns when required.
- Organized course-wise logging for easy data management.

### **Real-Time LCD Feedback**
- Displays current mode (REG/ATC)
- Shows messages such as:
  - *“Attendance Marked”*  
  - *“Not Registered”*  
  - *“Already Marked Today”*  
  - *“WiFi Disconnected”*  

### **User-Friendly Navigation**
- Hardware buttons allow switching between modes and selecting courses.
- Smooth interaction flow with clear on-screen prompts.

---

## 🧩 System Workflow

1. **User taps NFC card**  
2. ESP32 reads card UID via PN532  
3. Device sends UID + selected course to Google Apps Script  
4. Script:
   - Verifies registration  
   - Checks duplicate attendance  
   - Logs data to Google Sheets  
5. ESP32 shows confirmation or error on LCD

---

## 🛠 Tech Stack

- **Hardware:** ESP32, PN532 NFC Module, 16×2 I2C LCD, Push Buttons  
- **Software:** Arduino IDE, Google Apps Script, Google Sheets  
- **Connectivity:** Wi-Fi integration for cloud sync  

---

## 🎨 UI & Interaction Design

- Clear, minimal LCD interface for instructions and feedback  
- Mode selection and course navigation using tactile push buttons  
- Smooth real-time updates upon each successful NFC scan  
- Indicates every system state (success, error, duplicate scan, Wi-Fi issues)

---

## Snapshots

<img width="653" height="905" alt="image" src="https://github.com/user-attachments/assets/3c163962-70f0-468b-9c93-8602d8fc3d07" />
<img width="734" height="623" alt="image" src="https://github.com/user-attachments/assets/6aa44dfb-a831-4fb0-8eaf-5d64c1c74754" />
<img width="555" height="194" alt="image" src="https://github.com/user-attachments/assets/b50ba120-bf3c-47b8-8071-43e4de64dec9" />


## 📘 Summary

This NFC-based attendance system demonstrates real-world integration of embedded hardware and cloud services, offering a fast, reliable, and user-friendly way to manage attendance. With automated NFC card scanning, Google Sheets synchronization, and responsive LCD feedback, the project provides an efficient alternative to manual logging, ideal for classrooms, labs, and small institutions.


