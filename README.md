# Team Task Manager (Full-Stack)

Role-based task manager where teams can create projects, assign tasks, and track progress.

## Features

- Authentication (signup/login) using JWT
- Role-based access control (`ADMIN`, `MEMBER`)
- Project and team management
- Task creation, assignment, status tracking (`TODO`, `IN_PROGRESS`, `DONE`)
- Dashboard metrics (total, todo, in-progress, done, overdue)
- REST APIs + relational database (Prisma + PostgreSQL)

## Tech Stack

- Backend: Node.js, Express, Prisma, PostgreSQL
- Frontend: Vanilla JS SPA served by Express
- Validation: Zod
- Auth: JWT + bcrypt

## API Overview

- `POST /api/auth/signup`
- `POST /api/auth/login`
- `GET /api/auth/me`
- `GET /api/users` (admin)
- `GET /api/projects`
- `POST /api/projects` (admin)
- `GET /api/tasks`
- `POST /api/tasks` (admin)
- `PATCH /api/tasks/:id`
- `GET /api/dashboard`

## Local Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Create/update environment file (`.env`):
   ```env
   DATABASE_URL="postgresql://postgres:postgres@localhost:5432/team_task_manager?schema=public"
   JWT_SECRET="super-secret-change-in-production"
   PORT=5000
   ```

3. Create DB schema and Prisma client:
   ```bash
   npm run db:push
   npm run db:generate
   ```

4. (Optional) Seed demo users/projects/tasks:
   ```bash
   npm run seed
   ```

5. Start app:
   ```bash
   npm run dev
   ```

6. Open:
   - [http://localhost:5000](http://localhost:5000)


