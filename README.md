# 🎥 Video Conferencing App

A full-stack **Zoom-like video conferencing web application** that enables users to communicate in real time through video and audio, join meeting rooms, and interact with other participants.

The project is built with a React frontend and a Node.js/Express backend, with real-time communication handled using WebRTC and Socket.IO.

---

## 🌐 Live Demo

### 🎥 Frontend

https://video-conferencing-frontend-tu7z.onrender.com

### ⚙️ Backend

https://video-conferencing-backend-gys7.onrender.com

### 💻 GitHub Repository

https://github.com/Gaurangi2904/Video-Conferencing-App

---

## 📌 About The Project

This project is a Zoom-inspired video conferencing application created to understand how real-time communication works in a full-stack web application.

Users can enter a meeting, enable their camera and microphone, communicate with other participants, and use real-time collaboration features.

The application uses:

* React for the frontend
* Node.js and Express for the backend
* WebRTC for real-time audio/video communication
* Socket.IO for real-time signaling and communication

---

## ✨ Features

### 🎥 Video & Audio Calling

* Real-time video communication
* Real-time audio communication
* Camera on/off
* Microphone mute/unmute
* Multiple participants

### 🖥️ Screen Sharing

Users can share their screen with other participants during a meeting.

### 💬 Real-Time Chat

Participants can communicate through a real-time chat system while attending a meeting.

### 👥 Meeting Rooms

Users can join a meeting room and communicate with other participants in the same room.

### 🔄 Real-Time User Presence

The application handles users joining and leaving meeting rooms in real time.

### 🛑 End Call

Users can leave the meeting and stop their camera and microphone streams.

### 🔐 Authentication

The application includes authentication functionality to provide controlled access to the conferencing application.

---

# 🛠️ Tech Stack

## Frontend

* React.js
* JavaScript
* Material UI
* Socket.IO Client
* WebRTC
* CSS

## Backend

* Node.js
* Express.js
* Socket.IO
* JavaScript

## Real-Time Communication

* WebRTC
* Socket.IO

## Deployment

* Render
* GitHub

---

# 🏗️ System Architecture

```text
                   👤 User
                     │
                     ▼
          ┌─────────────────────┐
          │   React Frontend    │
          │      Render         │
          └──────────┬──────────┘
                     │
                     │ HTTP / Socket.IO
                     ▼
          ┌─────────────────────┐
          │  Node.js + Express  │
          │      Backend        │
          └──────────┬──────────┘
                     │
                     │ Signaling
                     ▼
          ┌─────────────────────┐
          │     Socket.IO       │
          │  Real-Time Events   │
          └──────────┬──────────┘
                     │
                     ▼
          ┌─────────────────────┐
          │       WebRTC        │
          │ Audio / Video Media  │
          └──────────┬──────────┘
                     │
              Peer-to-Peer Media
                     │
          ┌──────────▼──────────┐
          │  Other Participants │
          └─────────────────────┘
```

---

# 🔄 How the Application Works

The application uses **Socket.IO for signaling** and **WebRTC for peer-to-peer media communication**.

The basic flow is:

```text
User opens application
        ↓
Enters meeting information
        ↓
Connects to Socket.IO server
        ↓
Joins meeting room
        ↓
Socket.IO exchanges signaling information
        ↓
WebRTC establishes peer connections
        ↓
Camera + Microphone streams are shared
        ↓
Participants communicate in real time
```

---

# 🌐 WebRTC

WebRTC is responsible for the actual real-time media communication.

It allows browsers to communicate directly for:

* 🎥 Video
* 🎤 Audio
* 🖥️ Screen sharing

The application uses browser APIs such as:

```javascript
navigator.mediaDevices.getUserMedia()
```

to access the camera and microphone.

For screen sharing, the browser provides:

```javascript
navigator.mediaDevices.getDisplayMedia()
```

WebRTC handles the media connection between participants.

---

# 🔌 Socket.IO

Socket.IO is used as the real-time communication/signaling layer.

It helps the application:

* Connect users to meeting rooms
* Notify users when someone joins
* Notify users when someone leaves
* Exchange WebRTC signaling information
* Send real-time chat messages
* Maintain participant presence

The important distinction is:

```text
Socket.IO
    ↓
Signaling / real-time events

WebRTC
    ↓
Actual audio/video communication
```

---

# 📂 Project Structure

```text
Video-Conferencing-App/
│
├── backend/
│   ├── src/
│   ├── package.json
│   └── ...
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── .gitignore
└── README.md
```

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/Gaurangi2904/Video-Conferencing-App.git
```

```bash
cd Video-Conferencing-App
```

---

# ⚙️ Backend Setup

Navigate to the backend:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Start the backend:

```bash
npm start
```

The backend will run on the configured local port.

---

# 🎨 Frontend Setup

Open another terminal and navigate to the frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the frontend:

```bash
npm start
```

Open the application in your browser.

---

# 🔐 Environment Variables

Create the required environment variables according to the configuration used by the application.

Example:

```env
PORT=8000
```

If your application uses additional environment variables, add them to your local `.env` file.

⚠️ Never commit passwords, API keys, tokens, or other secrets to GitHub.

---

# ☁️ Deployment

The project is deployed on Render.

| Part     | Platform | URL                                                   |
| -------- | -------- | ----------------------------------------------------- |
| Frontend | Render   | https://video-conferencing-frontend-tu7z.onrender.com |
| Backend  | Render   | https://video-conferencing-backend-gys7.onrender.com  |

---

# 🧠 Key Concepts Learned

Through this project, I gained practical experience with:

* React.js
* Node.js
* Express.js
* WebRTC
* Socket.IO
* Real-time communication
* WebRTC signaling
* Peer-to-peer communication
* Camera and microphone APIs
* Screen sharing
* Meeting rooms
* Client-server architecture
* REST APIs
* CORS
* Git and GitHub
* Render deployment

---

# 🎯 Project Objective

The main objective of this project was to understand how modern video conferencing applications work and how real-time communication can be implemented using WebRTC and Socket.IO.

The project helped me understand the difference between:

```text
HTTP
↓
Request / Response communication
```

and:

```text
WebSocket / Socket.IO
↓
Real-time communication
```

as well as:

```text
WebRTC
↓
Real-time audio/video communication
```

---

# 🔮 Future Improvements

Some improvements planned for future versions include:

* 🔐 Improved authentication and authorization
* 👤 User profiles
* 🗓️ Meeting scheduling
* 📝 Meeting history
* ☁️ Cloud recording
* 💬 Improved chat functionality
* 👥 Participant management
* 🔗 Shareable meeting links
* 📱 Better mobile responsiveness
* 🎙️ Better audio controls
* 🖥️ Improved screen sharing
* 🛡️ Improved security

---

# 👩‍💻 Author

### Gaurangi Kapare

Full Stack Web Developer

GitHub:
https://github.com/Gaurangi2904

---

## ⭐ Project

**Video Conferencing App — A full-stack real-time video conferencing application built with React, Node.js, Socket.IO and WebRTC.**
