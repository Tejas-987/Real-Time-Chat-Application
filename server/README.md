
# 🗨️ Chatters – Backend

This is the **backend server** for the Chatters real-time chat application, built with **Node.js**, **Express**, **MongoDB**, and **Socket.io**. The backend provides REST APIs, JWT authentication, real-time messaging, file upload capabilities, and is containerized using **Docker**.

---

## 🛠️ Tech Stack

- **Node.js** – JavaScript runtime
- **Express.js** – Backend web framework
- **MongoDB** – NoSQL database with Mongoose
- **Socket.io** – Real-time WebSocket communication
- **Redis** – Pub/Sub and user presence
- **JWT (jsonwebtoken)** – Authentication
- **Multer** – File uploads
- **bcrypt** – Password hashing
- **dotenv** – Environment variable management
- **cookie-parser** – Cookie handling

---

## 📁 Folder Structure

```

server/
├── config/            # MongoDB & Redis setup
├── controllers/       # Route handlers
├── middlewares/       # Auth & error handling
├── models/            # Mongoose schemas
├── routes/            # API endpoints
├── sockets/           # Socket.io logic
├── uploads/           # Uploaded files
├── .env               # Environment variables
├── Dockerfile         # Docker build definition
└── index.js           # Entry point

````



## 🚀 Running Locally

1. Install dependencies:

```bash
npm install
```

2. Start development server:

```bash
npm run dev
```

Backend runs at: [http://localhost:8080](http://localhost:8080)

---

## 🐳 Running with Docker

To containerize the backend using the `Dockerfile`:

### 1. Build the Docker image:

```bash
docker build -t chat-app-server .
```

### 2. Run the container:

```bash
docker run -p 8080:8080 --env-file .env chat-app-server
```

Make sure MongoDB and Redis are available and reachable by the container.

---

## 🔌 API Endpoints

| Method | Endpoint            | Description          |
| ------ | ------------------- | -------------------- |
| POST   | `/api/auth/signup`  | Register a new user  |
| POST   | `/api/auth/login`   | Authenticate a user  |
| GET    | `/api/messages/:id` | Fetch messages by ID |
| POST   | `/api/messages`     | Send a new message   |
| POST   | `/api/group/create` | Create a group chat  |

---

## 📄 Notes

* MongoDB must be running on `localhost:27017` or configured using environment variables.
* Redis should be running for full real-time capabilities.
* Uploaded files are saved to `uploads/` and served via static routes.

---

```

