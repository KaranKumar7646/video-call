# 🎥 Video Conferencing Platform

A real-time video conferencing web app built with the **MERN stack** and **WebRTC**. Users can join multi-person meetings, chat live, and share their screen, all directly in the browser.

🔗 **Live Demo:** [video-callfrontend-meho.onrender.com](https://video-callfrontend-meho.onrender.com/)

> ⏳ The app is hosted on Render's free tier, so the first load may take 30 to 60 seconds to wake up.

<!--
Add screenshots here after uploading them to a /screenshots folder, e.g.:
![Home page](screenshots/home.png)
![Meeting room](screenshots/meeting.png)
-->

---

## ✨ Features

- 📹 **Peer-to-peer video calls** using WebRTC
- 👥 **Multi-user meetings** in a shared room
- 💬 **Live chat** during a meeting (Socket.io)
- 🖥️ **Screen sharing**
- 🔐 **Secure sessions** with bcrypt password hashing
- 🌐 **Deployed live** on Render

---

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React.js, JavaScript, CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB (Mongoose) |
| Real-time | WebRTC, Socket.io (signaling server) |
| Security | bcrypt |
| Deployment | Render |

---

## 🧠 How It Works

1. A user opens the app and joins a meeting room.
2. **Socket.io** acts as the signaling server. It exchanges connection details (offers, answers, ICE candidates) between users.
3. Once signaling is done, **WebRTC** creates direct peer-to-peer connections so audio and video stream between browsers without passing through the server.
4. Chat messages travel through Socket.io in real time.

---

## 📁 Project Structure

```
video-call/
├── backend/     # Express server, Socket.io signaling, MongoDB models
└── frontend/    # React client (meeting UI, chat, screen share)
```

---

## 🚀 Run It Locally

### Prerequisites
- Node.js (v16 or higher)
- A MongoDB database (local or MongoDB Atlas)

### 1. Clone the repository
```bash
git clone https://github.com/KaranKumar7646/video-call.git
cd video-call
```

### 2. Set up the backend
```bash
cd backend
npm install
```
Create a `.env` file inside `backend/` with your own values (check the backend code for the exact variable names):
```env
MONGO_URL=your_mongodb_connection_string
PORT=8000
```
Start the server:
```bash
npm start
```

### 3. Set up the frontend
Open a new terminal:
```bash
cd frontend
npm install
npm start
```
Update the backend URL in the frontend config if needed, then open the app in your browser.

---

## 🔮 Future Improvements

- Meeting links and scheduling
- Waiting room and host controls
- Recording meetings
- TURN server for better connectivity behind strict firewalls

---

## 👤 Author

**Karan Kumar**
[GitHub](https://github.com/KaranKumar7646) · [LinkedIn](https://www.linkedin.com/in/karan-kumar-687854282/)

⭐ If you found this project useful, consider giving it a star!
