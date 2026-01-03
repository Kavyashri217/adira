## High-Level Architecture (JavaScript-centric)
Frontend → React (UI, learning content, dashboards)

Backend → Node.js + Express (APIs, auth, logic)

Database → MongoDB / PostgreSQL (users, lessons, progress)

Auth → JWT / OAuth (secure login)

Hosting → Vercel (frontend) + Render/Railway (backend)

## Basic Folder Structure

Root Project
```text
empowerment/
│
├── client/        # Frontend (React)
├── server/        # Backend (Node + Express)
├── README.md
├── .gitignore

```text
Frontend(React)
client/
│
├── public/
│   └── index.html
│
├── src/
│   ├── assets/           # images, icons
│   ├── components/       # reusable UI components
│   │   ├── Navbar.js
│   │   ├── Footer.js
│   │   └── LessonCard.js
│   │
│   ├── pages/            # full pages
│   │   ├── Home.js
│   │   ├── Learn.js
│   │   ├── BudgetPlanner.js
│   │   ├── Login.js
│   │   └── Profile.js
│   │
│   ├── services/         # API calls
│   │   └── api.js
│   │
│   ├── context/          # global state
│   │   └── AuthContext.js
│   │
│   ├── utils/            # helper functions
│   │   └── formatCurrency.js
│   │
│   ├── App.js
│   └── index.js
│
├── package.json

```text
Backend Structure (Node.js + Express)
server/
│
├── src/
│   ├── controllers/      # request logic
│   │   ├── authController.js
│   │   ├── lessonController.js
│   │   └── userController.js
│   │
│   ├── routes/           # API routes
│   │   ├── authRoutes.js
│   │   ├── lessonRoutes.js
│   │   └── userRoutes.js
│   │
│   ├── models/           # database schemas
│   │   ├── User.js
│   │   └── Lesson.js
│   │
│   ├── middleware/       # auth, validation
│   │   └── authMiddleware.js
│   │
│   ├── utils/            # helpers
│   │   └── generateToken.js
│   │
│   ├── app.js            # express app
│   └── server.js         # entry point
│
├── .env
├── package.json

## Core Features (Mapped to Structure)
| Feature           | Frontend           | Backend             |
| ----------------- | ------------------ | ------------------- |
| Financial lessons | `pages/Learn.js`   | `lessonRoutes.js`   |
| Budget calculator | `BudgetPlanner.js` | utils / services    |
| User login        | `Login.js`         | `authController.js` |
| Progress tracking | `Profile.js`       | `userController.js` |

## JS Libraries that is likely used 
Frontend:

react
react-router-dom
axios
chart.js → visualize savings & spending
tailwindcss or mui → clean UI

Backend:
express
jsonwebtoken
bcrypt
mongoose or prisma
cors

