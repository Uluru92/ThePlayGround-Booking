# ThePlayGround-Booking
App focused on registering and follow every class booking for a gym with diferent kind of classes and teachers.

# 🏋️‍♀️ Gym Manager App — Hojancha Guanacaste

A modern and community-focused gym management application built for local gyms in Guanacaste, Costa Rica.  
The app combines **Google AppSheet** (for the frontend and user interface) with a **Python backend** for automation, notifications, and data control.

---

## 🌿 Overview

**Gym Manager App** is designed to give gym users an enjoyable and motivating experience while keeping operations simple for administrators and instructors.

The app provides:
- A visually pleasant interface focused on wellness and motivation.
- Class scheduling up to 30 days in advance.
- Participant registration and seat tracking.
- Instructor notes and dynamic communication.
- Role-based access (Admin, Professor, Student).
- Integration with Google Drive / Google Sheets for data persistence.

---

## 🧱 Project Structure

---

## 🧩 Roles & Features

### 👑 Administrator
- Add or remove instructors.
- View student payments and class statistics.
- Manage users and permissions.
- Update gym information and images.

### 🧘 Instructor
- Create, edit, and delete their own classes.
- Add class notes or updates.
- View participants and attendance.
- Upload their profile picture.

### 🏃 Student
- View the next 30 days of active classes.
- Register or cancel attendance.
- View class details, instructor, and participants.
- Upload payment receipts.
- Edit profile name and photo.

---

## 💾 Data Model (Google Sheets)

Each Google Sheet acts as a lightweight database for AppSheet.

| Table | Description |
|--------|--------------|
| `Users` | Stores user profiles and roles (admin / professor / student). |
| `Classes` | Contains all scheduled classes with title, date, time, instructor, capacity, and participants. |
| `Attendance` | Tracks each student's attendance status. |
| `Payments` | Stores uploaded payment receipts and transaction data. |
| `Notifications` | Used by backend to notify users of class openings. |

---

## ⚙️ Backend Overview (Python)

- Built with **FastAPI** (or Flask) for simplicity.
- Handles:
  - Webhooks from AppSheet (for real-time updates).
  - Notifications (email or WhatsApp) when a class spot opens.
  - Secure storage and backup of Google Sheets data.
- Optional connection to PostgreSQL for advanced analytics.
