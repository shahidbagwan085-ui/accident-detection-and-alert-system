# 🚨 Accident Detection & Alert System

A real-time web application that detects road accidents, displays live alerts on an interactive map, and notifies emergency responders — built with Node.js, Express, and MongoDB.

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
  - [Running the App](#running-the-app)
- [Pages & Screens](#pages--screens)
- [Authentication](#authentication)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

---

## 📌 About the Project

The **Accident Detection & Alert System** is a full-stack web application designed to improve road safety by providing real-time accident detection, live map visualization, and instant alerts. It supports user authentication (standard login + Google OAuth), a live dashboard with accident severity tracking, and a historical log of past incidents.

---

## ✨ Features

- 🗺️ **Live Accident Map** — Interactive map powered by Leaflet.js showing real-time accident locations
- ⚠️ **Real-Time Alerts** — Instant accident notifications with location, time, and severity
- 📜 **Accident History** — Full historical log with date, time, location, and severity level
- 🔐 **User Authentication** — Secure login/signup with JWT + Google OAuth support
- 🌙 **Dark Mode** — Toggle between light and dark themes
- 📱 **Responsive Design** — Works seamlessly on desktop and mobile devices
- 👤 **User Profile** — Manage personal account details
- 🎨 **Modern UI** — Built with Tailwind CSS, Poppins font, and smooth animations

---

## 🛠️ Tech Stack

| Layer      | Technology                          |
|------------|-------------------------------------|
| Frontend   | HTML5, CSS3, JavaScript, Tailwind CSS |
| Backend    | Node.js, Express.js                 |
| Database   | MongoDB (via Mongoose)              |
| Auth       | JWT (JSON Web Tokens), Google OAuth |
| Map        | Leaflet.js                          |
| Icons      | Font Awesome 6                      |
| Fonts      | Google Fonts (Poppins)              |

---

## 📁 Project Structure

```
accident-detection-system/
│
├── server.js           # Express server entry point
├── db.js               # MongoDB connection setup
├── auth.js             # Authentication routes (login, signup, Google OAuth)
├── profile.js          # User profile routes
├── User.js             # Mongoose User model
├── package.json        # Project dependencies & scripts
├── .env                # Environment variables (not committed to Git)
│
├── index.html          # Main dashboard page (live map + alerts)
├── dashbord.html       # Extended dashboard with analytics
└── login.html          # Login / Signup page
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/) (local or Atlas cloud)
- npm (comes with Node.js)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/accident-detection-system.git
   cd accident-detection-system
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

### Environment Variables

Create a `.env` file in the root directory and add the following:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
GOOGLE_CLIENT_ID=your_google_oauth_client_id
GOOGLE_CLIENT_SECRET=your_google_oauth_client_secret
```

> ⚠️ **Never commit your `.env` file to GitHub.** It is already listed in `.gitignore`.

### Running the App

**Development mode:**

```bash
npm run dev
```

**Production mode:**

```bash
npm start
```

Then open your browser and go to:

```
http://localhost:5000
```

---

## 🖥️ Pages & Screens

| Page              | File             | Description                                      |
|-------------------|------------------|--------------------------------------------------|
| Landing / Login   | `login.html`     | Login and signup page with Google OAuth option   |
| Main Dashboard    | `index.html`     | Live map, real-time alerts, accident history     |
| Extended Dashboard| `dashbord.html`  | Advanced analytics and incident management       |

---

## 🔐 Authentication

This project supports two authentication methods:

1. **Email & Password** — Standard login with JWT token-based sessions
2. **Google OAuth** — One-click login using your Google account

Tokens are stored securely and used to protect private routes (profile, dashboard).

---

## 📡 API Endpoints

| Method | Endpoint            | Description                    | Auth Required |
|--------|---------------------|--------------------------------|---------------|
| POST   | `/api/auth/signup`  | Register a new user            | No            |
| POST   | `/api/auth/login`   | Login and receive JWT token    | No            |
| GET    | `/api/auth/google`  | Initiate Google OAuth flow     | No            |
| GET    | `/api/profile`      | Get logged-in user profile     | Yes           |
| PUT    | `/api/profile`      | Update user profile            | Yes           |

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "Add your feature"`
4. Push to your branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please make sure your code is clean and well-commented.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

Made with ❤️ by **[Your Name](https://github.com/your-username)**

---

> ⭐ If you found this project helpful, please give it a star on GitHub!
