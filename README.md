# ⚡ Syncra Edge

**The Resilient, Offline-First Attendance System for Madagascar.**

Syncra Edge is a high-performance school management solution designed to keep classrooms running even when the international internet connection fails. Built with a **Go** edge-server and a **React/TS** dashboard, it treats "Offline" as a first-class citizen.

---

## 🌍 The Problem
In many educational institutions in Madagascar (like HEI or Ankatso), cloud-based tools (Google Meet, web-based attendance) often become inaccessible due to frequent internet outages. This disrupts the pedagogical workflow, even when students and teachers are on the same local network (LAN).

## 💡 The Solution
**Syncra Edge** acts as a local bridge. It allows teachers to perform attendance and manage classroom data on a local server.
- **Offline Mode:** Data is stored locally in an optimized **SQLite** database.
- **Automatic Sync:** As soon as connectivity is restored, the system intelligently pushes local updates to the Cloud.
- **Local Network Discovery:** Uses mDNS so students can find the local hub without an internet connection.

## 🛠️ Tech Stack

- **Frontend:** React 19, TypeScript, Tailwind CSS (Glassmorphism UI).
- **Backend (Edge):** Go (Golang) for high-performance local concurrency.
- **Database:** SQLite (Local) & PostgreSQL (Cloud Sync).
- **Infrastructure:** Docker & Docker Compose for rapid deployment.
- **Communication:** WebSockets for real-time status updates.

## 🚀 Key Features

- [x] **Zero-Data Attendance:** Take attendance over the local Wi-Fi.
- [x] **Smart Sync Engine:** Automatic background synchronization to the cloud.
- [x] **Connectivity Dashboard:** Visual indicators for "Local Only" vs "Cloud Synced" status.
- [x] **PWA Support:** Installable on mobile devices for quick access.

## 📂 Project Structure

```text
syncra-edge/
├── client/           # React + TS Frontend (SaaS Dashboard)
├── server/           # Go Backend (Edge & Sync Logic)
├── docker/           # Containerization & Deployment
└── figma/            # Design System & Style Guide
