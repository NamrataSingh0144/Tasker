README.txt
================================================================
TASKER — Team Task Manager
================================================================
 
LIVE URL:
https://frontend-production-0dd4.up.railway.app
 
GITHUB REPOSITORY:
https://github.com/NamrataSingh0144/Tasker
 
================================================================
WHAT IS TASKER?
================================================================
Tasker is a team task management app I built to help teams
stay organized. The idea is simple — you create projects,
add tasks, assign them to teammates, and everyone can track
what's done, what's in progress, and what's overdue.
 
It has role-based access, so Admins have full control while
Members can focus on their assigned work. The first person
to register automatically becomes the Admin.
 
================================================================
WHAT CAN YOU DO WITH IT?
================================================================
- Sign up and log in securely
- Create projects and organize work
- Add tasks with due dates, priorities, and assignees
- Update task status (Todo → In Progress → Done)
- See overdue tasks that need attention
- Get a dashboard overview of everything happening
- Admin can manage the whole team; Members see their work
 
================================================================
TECH I USED
================================================================
Frontend:
  React, TypeScript, Vite, Tailwind CSS,
  React Router, Axios, Lucide Icons
 
Backend:
  Node.js, Express, TypeScript, MongoDB, Mongoose,
  JWT for auth, Bcrypt for password hashing
 
Deployed on Railway (frontend + backend)
Database on MongoDB Atlas
 
================================================================
HOW TO RUN IT LOCALLY
================================================================
You'll need Node.js v18+ and a MongoDB Atlas connection string.
 
Step 1 — Clone the repo:
  git clone https://github.com/NamrataSingh0144/Tasker.git
  cd Tasker
 
Step 2 — Start the backend:
  cd backend
  npm install
  Create a .env file and add:
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=any_secret_key
    PORT=5000
  npm run dev
 
Step 3 — Start the frontend:
  cd frontend
  npm install
  Create a .env file and add:
    VITE_API_URL=http://localhost:5000/api
  npm run dev
 
Step 4 — Open http://localhost:5173 in your browser.
  The first account you create will be Admin.
 
================================================================
PROJECT STRUCTURE
================================================================
assignment/
├── frontend/          # React app (UI, pages, components)
└── backend/           # Express API (routes, models, auth)
 
================================================================
API ROUTES
================================================================
POST   /api/auth/register        Register a new user
POST   /api/auth/login           Login
 
GET    /api/projects             List all projects
POST   /api/projects             Create a project (Admin)
GET    /api/projects/:id         Get project details
DELETE /api/projects/:id         Delete a project (Admin)
 
GET    /api/tasks                List all tasks
POST   /api/tasks                Create a task (Admin)
PATCH  /api/tasks/:id            Update task status
DELETE /api/tasks/:id            Delete a task (Admin)
GET    /api/tasks/dashboard      Dashboard stats
 
================================================================
DEPLOYMENT
================================================================
I deployed both services on Railway.
 
Backend: https://tasker-production-ff33.up.railway.app
Frontend: https://frontend-production-0dd4.up.railway.app
 
================================================================
AUTHOR
================================================================
Namrata Singh
GitHub: https://github.com/NamrataSingh0144/Tasker
 
================================================================
