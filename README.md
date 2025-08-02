
# 💬 Chatters – Real-Time Chat Application

Chatters is a full-stack real-time chat application built with **Next.js, Node.js, Express, MongoDB, Socket.io**, and **Redis**. It supports **real-time messaging**, **group chats**, **file sharing**, and **JWT-based authentication** with Docker support for containerized deployment.

---

## 🚀 Tech Stack

### 🖥️ Frontend
- **Next.js** 14
- **React** 18
- **Zustand** (State Management)
- **Socket.io Client**
- **Axios** (API requests)
- **Day.js** (Date formatting)
- **React Markdown + Remark GFM**
- **GSAP + @gsap/react** (UI animations)

### 🛠️ Backend
- **Node.js + Express**
- **MongoDB + Mongoose**
- **Redis** (Pub/Sub + Presence)
- **Socket.io**
- **JWT** (Authentication)
- **Multer** (File Uploads)
- **Bcrypt** (Password Hashing)
- **dotenv + cookie-parser**

---

## 🏗️ Project Structure

```

chatters/
├── client/          # Next.js frontend
├── server/          # Express backend
├── docker-compose.yml
├── package.json     # Monorepo scripts
└── README.md

````

---

## 🧩 Features

- ✅ JWT-based authentication
- 💬 Real-time one-on-one and group chat
- 📁 File upload and sharing
- 👁️ Online/offline presence (Redis)
- 📜 Markdown support in messages
- 🔐 Role-based access to groups
- 🐳 Full Docker setup for deployment

---

## ⚙️ Setup Instructions

### 📦 Manual Setup

```bash
# Clone the repo
git clone https://github.com/Tejas-987/Real-Time-Chat-Application
cd chatters-realtime-chat-app

# Install dependencies
npm run install:all

# Start dev servers
npm run dev
````

### 🔐 Environment Variables

#### server/.env

```env
PORT=8080
JWT_KEY=your-jwt-secret
DATABASE_URL=mongodb://localhost:27017/chat-app
REDIS_HOST=localhost
REDIS_PORT=6379
```

#### client/.env.local

```env
NEXT_PUBLIC_SERVER_URL=http://localhost:8080
```

---

## 🐳 Docker Setup

Make sure Docker and Docker Compose are installed.

```bash
docker-compose up --build
```

* Frontend: `http://localhost:3000`
* Backend: `http://localhost:8080`
* MongoDB: `localhost:27017`
* Redis: `localhost:6379`

---

## 📡 API Endpoints

| Method | Endpoint           | Description             |
| ------ | ------------------ | ----------------------- |
| POST   | /api/auth/signup   | Register new user       |
| POST   | /api/auth/login    | User login              |
| GET    | /api/messages/\:id | Get chat messages       |
| POST   | /api/messages      | Send a new message      |
| POST   | /api/group/create  | Create a new group chat |


