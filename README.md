# 👗 StyleSense – AI-Powered Fashion Recommendation System

StyleSense is an intelligent fashion recommendation platform that helps users discover outfits tailored to their skin tone, occasion, budget, gender, and personal style preferences. By combining MediaPipe, OpenCV, MongoDB, Flask, React, and Groq LLM, the system delivers smart styling suggestions, shopping recommendations, and an AI-powered fashion assistant.

---

## ✨ Key Features

### 🔐 Secure Authentication
- JWT-based user authentication
- User registration and login
- Protected routes and personalized profiles

### 📸 Skin Tone Detection
- Upload image or capture through webcam
- Face detection using MediaPipe
- Skin tone analysis using OpenCV
- Personalized color palette generation

### 👔 AI Outfit Recommendations
- Occasion-based outfit suggestions
- Budget-aware recommendations
- Skin-tone matched color combinations
- Personalized styling advice

### 🧥 Build Around My Item
- Upload an existing clothing item
- Generate matching outfit combinations
- Smart budget allocation for complementary items

### 🤖 AI Fashion Chatbot
- Powered by Groq LLM
- Fashion-focused conversations
- Outfit styling guidance
- Color matching recommendations

### 🛍️ Shopping Suggestions
Direct product search links for:
- Amazon
- Myntra
- Ajio
- Flipkart

### 💾 Saved Outfits & History
- Save favorite recommendations
- View previous styling sessions
- Access recommendation history

---

## 🏗️ System Architecture

```text
+----------------------+
|    React Frontend    |
+----------+-----------+
           |
           | REST APIs
           v
+----------------------+
|    Flask Backend     |
+-----+-----------+----+
      |           |
      |           v
      |      Groq LLM
      |
      v
+----------------------+
|   MongoDB Database   |
+----------------------+
           |
           v
+----------------------+
| MediaPipe + OpenCV   |
| Skin Tone Analysis   |
+----------------------+
```

---

## 🛠️ Technology Stack

### Frontend
- React.js
- React Router
- Axios

### Backend
- Flask
- Flask-CORS
- Bcrypt

### Database
- MongoDB Atlas
- PyMongo

### AI & Computer Vision
- Groq API
- Llama Models
- OpenCV
- MediaPipe
- NumPy
- Pillow

---

## 📁 Project Structure

```text
StyleSense/
│
├── backend/
│   ├── routes/
│   │   ├── auth.py
│   │   ├── photo.py
│   │   ├── outfit.py
│   │   ├── chatbot.py
│   │   └── profile.py
│   │
│   ├── utils/
│   │   ├── groq_ai.py
│   │   └── skin_tone.py
│   │
│   ├── middleware/
│   │   └── auth_middleware.py
│   │
│   ├── models/
│   │   └── user.py
│   │
│   ├── db.py
│   └── app.py
│
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   ├── context/
│   │   └── utils/
│   │
│   └── package.json
│
└── README.md
```


## ⚙️ Backend Setup

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create a `.env` file inside the backend folder:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
GROQ_API_KEY=your_groq_api_key
```

### Run Backend

```
python app.py
```

Backend runs on:

```
http://localhost:5000
```

---

## 💻 Frontend Setup

### Install Dependencies

```
cd frontend
npm install
```

### Configure Environment Variables

Create a `.env` file:

```env
VITE_API_URL=http://localhost:5000/api
```

### Run Frontend

```
npm run dev
```

Frontend runs on:

```
http://localhost:5173
```
