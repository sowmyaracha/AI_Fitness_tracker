
# 🏋️ AI Fitness Tracker

An intelligent, full-stack fitness tracking web application that helps users set goals, log workouts, monitor progress, and receive AI-powered recommendations — all in one place.

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [License](#license)
- [Author](#author)

---

## 📌 About the Project

**AI Fitness Tracker** is a full-stack web application designed to make fitness tracking smarter and more personalized. Users can register, log their daily workouts, set fitness goals, and track their progress over time. The AI component provides intelligent insights and recommendations based on activity data.

> Built with a **JavaScript frontend** and a **Node.js/Express backend**, this project follows a clean client-server architecture with a RESTful API.

---

## ✨ Features

- 🔐 **User Authentication** — Secure sign-up and login with JWT-based session management
- 🏃 **Workout Logging** — Log exercises with sets, reps, duration, and calories
- 🎯 **Goal Setting** — Set personalized fitness goals and track your milestones
- 📊 **Progress Dashboard** — Visual charts and stats to monitor your fitness journey
- 🤖 **AI Recommendations** — Smart workout and activity suggestions based on your history
- 🗓️ **Activity History** — View and manage past workout sessions
- 📱 **Responsive Design** — Mobile-friendly UI for tracking on the go

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| HTML5 | Markup structure |
| CSS3 | Styling and responsive layout |
| JavaScript (ES6+) | UI logic and API integration |

### Backend
| Technology | Purpose |
|---|---|
| Node.js | Server-side runtime |
| Express.js | RESTful API framework |
| MongoDB / Mongoose | Database and ODM |
| JSON Web Tokens (JWT) | Authentication |
| bcrypt | Password hashing |
| dotenv | Environment variable management |

---

## 📁 Project Structure

```
AI_Fitness_tracker/
├── backend/
│   ├── models/            # Mongoose data models (User, Workout, Goal, etc.)
│   ├── routes/            # API route handlers
│   ├── controllers/       # Business logic for each route
│   ├── middleware/        # Auth middleware (JWT verification)
│   ├── config/            # Database connection and config
│   ├── .env               # Environment variables (not committed)
│   ├── package.json
│   └── server.js          # Entry point for the backend server
│
├── frontend/
│   ├── index.html         # Main HTML entry point
│   ├── css/               # Stylesheets
│   ├── js/                # JavaScript modules and API calls
│   └── assets/            # Images and static resources
│
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (v16 or higher)
- [npm](https://www.npmjs.com/) (v7 or higher)
- [MongoDB](https://www.mongodb.com/) (local installation or a [MongoDB Atlas](https://www.mongodb.com/atlas) cloud cluster)

---

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/sowmyaracha/AI_Fitness_tracker.git
cd AI_Fitness_tracker
```

**2. Install backend dependencies**

```bash
cd backend
npm install
```

**3. Install frontend dependencies** *(if applicable)*

```bash
cd ../frontend
npm install
```

---

### Running the App

**1. Set up environment variables**

Create a `.env` file inside the `backend/` directory (see [Environment Variables](#environment-variables) below).

**2. Start the backend server**

```bash
cd backend
npm start
```

The backend will start on **http://localhost:5000** (or the port defined in your `.env`).

**3. Open the frontend**

Open `frontend/index.html` directly in your browser, or if using a dev server:

```bash
cd frontend
npm start
```

Then navigate to **http://localhost:3000** in your browser.

---

## 🔑 Environment Variables

Create a `.env` file in the `backend/` directory with the following variables:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRES_IN=7d
```

| Variable | Description |
|---|---|
| `PORT` | Port for the backend server |
| `MONGO_URI` | MongoDB connection URI (local or Atlas) |
| `JWT_SECRET` | Secret key for signing JWT tokens |
| `JWT_EXPIRES_IN` | Token expiry duration (e.g., `7d`, `24h`) |

> ⚠️ **Never commit your `.env` file.** It is already included in `.gitignore`.

---

## 📡 API Endpoints

### Auth Routes
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login and receive a JWT token |

### Workout Routes *(Protected)*
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/workouts` | Get all workouts for logged-in user |
| POST | `/api/workouts` | Log a new workout |
| PUT | `/api/workouts/:id` | Update a workout entry |
| DELETE | `/api/workouts/:id` | Delete a workout entry |

### Goal Routes *(Protected)*
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/goals` | Get all goals for logged-in user |
| POST | `/api/goals` | Create a new fitness goal |
| PUT | `/api/goals/:id` | Update a goal |
| DELETE | `/api/goals/:id` | Delete a goal |

> All protected routes require a valid JWT token in the `Authorization` header:
> ```
> Authorization: Bearer <your_token>
> ```

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please make sure your code follows the existing style and all tests pass before submitting.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👩‍💻 Author

**Sowmya Racha**

- GitHub: [@sowmyaracha](https://github.com/sowmyaracha)

---

> 💡 *If you found this project helpful, please consider giving it a ⭐ on GitHub!*
