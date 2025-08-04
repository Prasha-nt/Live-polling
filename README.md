# 📊 LivePoll: Real-Time Interactive Polling System

> Engage your audience like never before! A sleek, real-time polling application built with the modern web stack. Perfect for teachers, presenters, and anyone looking to create an interactive experience.



This application allows teachers to create polls on-the-fly and lets students vote and see live results instantly. It's packed with features like a real-time chat, participant management, and a full poll history.

---

## ✨ Key Features

A quick look at what you can do with LivePoll:

| Teacher Features 🧑‍🏫 | Student Features 👨‍🎓 |
| :--- | :--- |
| 📝 **Create Custom Polls** | ✅ **Join Instantly** |
| ⏱️ **Set Timers (15s - 120s)** | 🗳️ **Vote in Real-Time** |
| 📈 **View Live Results** | ⏳ **See Synchronized Timers** |
| 🚫 **Kick Participants** | 💬 **Engage in Live Chat** |
| 📜 **Access Poll History** | 🔄 **Persistent Name (in-tab)** |
| 💬 **Chat with Students** | 🔔 **Get Kick Notifications** |

---

## 🛠️ Tech Stack

This project is built with a powerful and modern tech stack to ensure a fast, reliable, and scalable experience.

| Category | Technology |
| :--- | :--- |
| **Frontend** | ⚛️ React,  Vite, 📘 TypeScript, 🔁 Redux Toolkit, 🌐 React Router, 🎨 Tailwind CSS |
| **Backend** | 🟩 Node.js, 🚀 Express.js |
| **Real-Time** | 🔌 Socket.IO (Client & Server) |
| **Database** | 🔥 Firebase / Firestore |

---

## 🏗️ System Architecture

The application uses a robust client-server architecture designed for seamless real-time communication.



### Data Flow Simplified
1.  **🧑‍🏫 Teacher Creates Poll:** The teacher submits a new poll from their dashboard.
2.  **☁️ Server & DB Magic:** The poll is saved to **Firebase** and broadcast via **Socket.IO** to all connected students.
3.  **👨‍🎓 Students Vote:** Students receive the poll instantly and submit their answers.
4.  **📈 Live Results For All:** The server processes votes, updates the results, and broadcasts them back to everyone in real-time!

---

## 🚀 Get Started

Ready to run your own instance? Follow these simple steps.

### Prerequisites
* Node.js (v16+)
* NPM or Yarn
* A Google Account for [Firebase](https://firebase.google.com/)

### Installation & Setup

1.  **Clone the Repository**
    ```bash
    git clone <repository-url>
    cd <repository-folder>
    ```

2.  **Install Dependencies**
    Install dependencies for both the frontend (root) and the backend (`server`).
    ```bash
    # Install frontend dependencies
    npm install

    # Install backend dependencies
    cd server
    npm install
    cd ..
    ```

3.  **Configure Firebase**
    * Create a new project on the [Firebase Console](https://firebase.google.com/).
    * Set up a **Firestore Database**.
    * In your project settings, find your Firebase configuration object.
    * Copy this configuration into the file `src/services/firebaseConfig.ts`.

4.  **Run the Application**
    You'll need two separate terminals for this.

    * **Terminal 1: Start the Backend Server**
        ```bash
        cd server
        npm start
        # Server is now running on http://localhost:3001
        ```

    * **Terminal 2: Start the Frontend App**
        ```bash
        # From the root directory
        npm run dev
        # App is now available at http://localhost:5173
        ```

---

## 🕹️ How to Use

### Teacher Flow
1.  Navigate to `http://localhost:5173/teacher`.
2.  Create a new poll with a question, options, and a timer.
3.  Click **Submit** to broadcast it to all students.
4.  Watch the results update live on your **Active Poll** screen!

### Student Flow
1.  Navigate to the root URL `http://localhost:5173/`.
2.  Enter a unique name to join the session.
3.  Wait for the teacher to start a poll.
4.  Select your answer before the timer runs out!

---

## License

This project is licensed under the **MIT License**.
