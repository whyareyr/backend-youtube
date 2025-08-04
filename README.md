# 🎬 YouTube Clone Backend

A complete backend for a YouTube-like video-sharing platform, built with **Node.js**, **Express**, and **MongoDB**. It handles authentication, video uploads & streaming, likes/dislikes, comments, and subscriptions.

## 🚀 Features

- 🔐 **User Authentication** – Secure signup/login with JWT.
- 📹 **Video Upload & Management** – Upload, update, and delete videos.
- 🎞️ **Video Streaming** – Stream videos efficiently.
- 👍 **Likes & Dislikes** – Like/dislike functionality.
- 💬 **Commenting System** – Add/delete comments.
- 📢 **Subscriptions** – Subscribe/unsubscribe to channels.
- 🔍 **Search & Filters** – Search by title, category, upload date, etc.

---

## 🛠️ Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB, Mongoose
- **Auth:** JWT (JSON Web Tokens)
- **File Handling:** Multer
- **Video Processing:** FFmpeg
- **Others:** dotenv, bcrypt

---

## 📁 API Endpoints

### 🔐 Authentication
- `POST /auth/signup` – Register user  
- `POST /auth/login` – Login and get JWT

### 📹 Videos
- `POST /videos/upload` – Upload a video  
- `GET /videos/:id` – Get video info and stream  
- `PUT /videos/:id` – Update video  
- `DELETE /videos/:id` – Delete video  
- `GET /videos/trending` – Trending videos

### 💬 Comments
- `POST /comments/:videoId` – Add comment  
- `GET /comments/:videoId` – Get comments  
- `DELETE /comments/:commentId` – Delete comment

### 👍 Likes & Dislikes
- `POST /videos/:id/like` – Like video  
- `POST /videos/:id/dislike` – Dislike video

### 📢 Subscriptions
- `POST /subscribe/:channelId` – Subscribe  
- `POST /unsubscribe/:channelId` – Unsubscribe  
- `GET /subscriptions` – Get feed from subscribed channels

---

## 🧾 Database Schema (Simplified)

### User
```json
{
  "username": "string",
  "email": "string",
  "password": "string",
  "subscribers": "number",
  "subscribedChannels": ["channelId"],
  "createdAt": "date"
}
