CivicPulse — AI Smart City Civic-Tech Platform
A modern full-stack civic-tech dashboard for citizens, BBMP officials, and municipal authorities to report, track, vote, and monitor public infrastructure issues.

Quick Start
Prerequisites
Node.js v18+ and npm v9+
Installation
bash

# 1. Install all dependencies (root + backend + frontend)
npm run install-all
# 2. Start both servers concurrently
npm run dev
Frontend: http://localhost:5173
Backend API: http://localhost:5000
No database installation required! The backend uses a local JSON file store by default. To connect MongoDB, create a .env file inside /backend with MONGODB_URI=your_connection_string.

Tech Stack
Layer	Technology
Frontend	React 18, Vite, Tailwind CSS, Framer Motion
Maps	Leaflet.js + CartoDB Dark Tiles
Charts	Recharts
Icons	Lucide React
Backend	Node.js, Express.js
Database	MongoDB (optional) / Local JSON fallback
Features
Interactive GIS Map — Dark-themed Leaflet map with severity-coded pulse markers, filter controls, and heatmap overlays
AI Duplicate Detection — Haversine + text similarity engine warns users of nearby active complaints
AI Priority Prediction — Keyword NLP auto-categorizes issues and predicts urgency levels
Gamification System — XP points, Bronze/Silver/Gold/Hero tiers, and community leaderboards
Admin Control Room — Officer dispatch, status pipeline management, and Recharts analytics
Dark/Light Mode — Full theme toggle with glassmorphism design system
Complaint Lifecycle Timeline — Visual tracker: Submitted → Verified → Assigned → In Progress → Resolved
Project Structure

civic-pulse-download/
├── package.json              # Root monorepo scripts
├── backend/
│   ├── package.json
│   ├── server.js             # Express bootstrap
│   ├── database.js           # Dual-mode DB (Mongo + JSON fallback)
│   ├── routes.js             # API routes + AI engines
│   └── data/                 # Auto-generated local JSON store
└── frontend/
    ├── package.json
    ├── index.html
    ├── vite.config.js
    ├── tailwind.config.js
    ├── postcss.config.js
    └── src/
        ├── main.jsx
        ├── App.jsx           # Router, navbar, notifications, theme
        ├── index.css          # Tailwind + glassmorphism design tokens
        └── pages/
            ├── Home.jsx       # Hero, stats, categories, live feed
            ├── MapPage.jsx    # Full-screen Leaflet GIS dashboard
            ├── ReportIssue.jsx# Smart complaint wizard + AI checks
            ├── Leaderboard.jsx# Gamification rankings
            ├── Profile.jsx    # Citizen dashboard + timeline
            └── Admin.jsx      # Municipal control room + charts
License
MIT — Built for civic empowerment.