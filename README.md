# CodeAlpha Task 2 – ConnectSphere Social Media Platform

## Technologies
HTML, CSS, vanilla JavaScript, Node.js, Express.js and MySQL. This project does not use React or Vite.

## Features
- Email/password registration and login; passwords hashed using bcryptjs
- User profile and editable bio
- Create posts with optional image URL
- Community feed, likes and comments
- Discover users and follow/unfollow
- MySQL tables for users, posts, comments, likes and follows

## Setup
1. Open MySQL Workbench and connect to your local MySQL server.
2. Open `database/connectsphere_db.sql`, copy all SQL and execute it. Refresh SCHEMAS and check `connectsphere_db`.
3. Copy `.env.example` to `.env` in the project root. Set `DB_PASSWORD` to your local MySQL password. Do not upload `.env` to GitHub.
4. Open VS Code terminal in the folder containing `package.json` and run:
   `npm install`
   `npm run dev`
5. Open http://localhost:5001
6. Register two accounts to test following, likes and comments.

## API
- POST `/api/auth/register`, POST `/api/auth/login`, GET `/api/auth/me`, POST `/api/auth/logout`
- GET/POST `/api/posts`, POST `/api/posts/:id/like`, POST `/api/posts/:id/comments`
- GET/PUT `/api/users/profile`, GET `/api/users/suggestions`, POST `/api/users/:id/follow`
- GET `/api/health`

The default Express session store is for local development only. Images are referenced by URL, not uploaded.