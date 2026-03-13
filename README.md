# 🔥 StreakLife

> **"Build streaks. Build yourself."**

A full-stack habit tracking web app that simplifies your daily health & wellness routine — track water intake, meals, steps, and diet with one-click logging and visual streak calendars.

---

## 📌 Problem Statement

People struggle to maintain consistent healthy habits like drinking enough water, eating balanced meals, tracking steps, and managing diet — due to complex apps and lack of visual progress feedback. **StreakLife** solves this by providing a frictionless one-click daily habit logger with visual streak tracking and diet monitoring — turning small daily actions into life-changing streaks.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React.js + Tailwind CSS |
| Backend | Node.js + Express.js |
| Database | MongoDB |
| Routing | React Router v6 |
| State Management | Context API |
| Charts | Recharts |

---

## ✨ Features

### 🏠 Core Modules
- 💧 **Water Intake** — Track daily glasses (goal: 8/day)
- 🍽️ **Meal Logging** — Log Breakfast, Lunch & Dinner
- 👣 **Step Counter** — Daily step count vs goal
- 🥗 **Diet Intake** — Track Calories, Protein, Carbs & Fats
- 🔥 **Streak Calendar** — Visual daily consistency tracker

### ✅ All 13 Mandatory Features
| # | Feature | Implementation |
|---|---|---|
| 1 | Routing & Navigation | React Router (Home, Login, Signup, Dashboard, Profile) |
| 2 | React Hooks | `useState`, `useEffect`, `useRef`, `useContext` |
| 3 | State Management | Context API (AuthContext + ThemeContext) |
| 4 | Authentication | Signup/Login + LocalStorage token + Protected Routes |
| 5 | Theme Support | Dark / Light mode toggle with persistence |
| 6 | Search, Filter & Sort | Search habits by name, filter by category, sort by streak |
| 7 | Debouncing | Debounced search bar for habits |
| 8 | Pagination | Paginated check-in history (backend limit/skip) |
| 9 | CRUD Operations | Create, Read, Update, Delete habits & check-ins |
| 10 | API Integration | REST APIs with loading states & error handling |
| 11 | Form Validation | Input validation with error messages on all forms |
| 12 | Responsive UI | Fully responsive with Tailwind CSS |
| 13 | Error Handling | Try-catch on all API calls + backend error middleware |

---

## 📁 Project Structure

```
streaklife/
├── client/                        # React Frontend
│   ├── public/
│   └── src/
│       ├── pages/
│       │   ├── Home.jsx
│       │   ├── Login.jsx
│       │   ├── Signup.jsx
│       │   ├── Dashboard.jsx
│       │   └── Profile.jsx
│       ├── components/
│       │   ├── Navbar.jsx
│       │   ├── HabitCard.jsx
│       │   ├── StreakCalendar.jsx
│       │   ├── SearchBar.jsx
│       │   └── Charts.jsx
│       ├── context/
│       │   ├── AuthContext.jsx
│       │   └── ThemeContext.jsx
│       └── hooks/
│           ├── useDebounce.js
│           └── useAuth.js
│
└── server/                        # Node.js + Express Backend
    ├── models/
    │   ├── User.js
    │   ├── Habit.js
    │   └── CheckIn.js
    ├── routes/
    │   ├── auth.js
    │   ├── habits.js
    │   └── checkins.js
    ├── middleware/
    │   ├── authMiddleware.js
    │   └── errorHandler.js
    └── index.js
```

---

## 🗄️ Database Models

```js
// User
{ name, email, password, theme, createdAt }

// Habit
{ userId, name, category, icon, targetPerDay, unit, streak, longestStreak, color }

// CheckIn
{ userId, habitId, date, value, note, calories, protein, carbs, fats }
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- MongoDB (local or Atlas)
- npm or yarn

### 1. Clone the repository
```bash
git clone https://github.com/your-username/streaklife.git
cd streaklife
```

### 2. Setup the Backend
```bash
cd server
npm install
```

Create a `.env` file inside `/server`:
```env
MONGO_URI=mongodb://localhost:27017/streaklife
JWT_SECRET=your_secret_key_here
PORT=5000
```

Start the server:
```bash
npm run dev
```

### 3. Setup the Frontend
```bash
cd ../client
npm install
npm run dev
```

### 4. Open in browser
```
http://localhost:5173
```

---

## 🔗 API Endpoints

### Auth
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/signup` | Register new user |
| POST | `/api/auth/login` | Login user |
| GET | `/api/auth/profile` | Get user profile |
| PUT | `/api/auth/profile` | Update profile |

### Habits
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/habits` | Get all habits (search/filter/sort/paginate) |
| POST | `/api/habits` | Create new habit |
| PUT | `/api/habits/:id` | Update habit |
| DELETE | `/api/habits/:id` | Delete habit |

### Check-ins
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/checkins/:habitId` | Get check-ins for a habit |
| GET | `/api/checkins/today/all` | Get today's check-ins |
| POST | `/api/checkins` | Log a check-in |
| DELETE | `/api/checkins/:id` | Delete a check-in |

---

## 🎨 Brand

- **Colors:** 🔥 Orange `#f97316` + 🌿 Green `#22c55e` + Dark `#09090b`
- **Fonts:** Syne (headings) + DM Sans (body)
- **Tagline:** *"Build streaks. Build yourself."*

---

## 👨‍💻 Team

Built with ❤️ at **Full Stack Hackathon**

---

## 📄 License

MIT License — feel free to use and modify!
