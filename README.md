🔐 RBAC Admin Dashboard

A Role-Based Access Control (RBAC) system built with Next.js to manage users, roles, and permissions in a secure and scalable way.

📌 What is RBAC?

RBAC decides who can do what in an application.

Users are assigned roles

Roles contain permissions

Permissions control allowed actions

This makes access control easy, secure, and organized.

🚀 Features

User Authentication (JWT)

User Management

Role Management

Permission Management

Role–Permission Mapping

User–Role Assignment

Protected API Routes

Admin Dashboard UI

🛠 Tech Stack

Frontend & Backend

Next.js (App Router)

TypeScript

Tailwind CSS

shadcn/ui

Database

PostgreSQL

Prisma ORM

Authentication

JWT

bcrypt

📂 Project Structure
app/
├── api/
│   ├── auth/
│   ├── users/
│   ├── roles/
│   ├── permissions/
│   └── role-permissions/
│
├── dashboard/
│   ├── users/
│   ├── roles/
│   ├── permissions/
│   └── role-permissions/
│
├── components/
│   ├── layout/
│   └── ui/
│
├── store/
│   └── rbacStore.ts
│
├── hooks/
├── lib/
│   └── prisma.ts
│
├── middleware.ts
└── page.tsx

🔧 Environment Variables

Create a .env file:

DATABASE_URL="postgresql://user:password@localhost:5432/rbac_db"
JWT_SECRET="your-secret-key"
JWT_EXPIRES_IN="24h"

📦 Installation & Setup
# Install dependencies
npm install

# Run database migrations
npx prisma migrate dev
npx prisma generate

# Start development server
npm run dev

📍 API Endpoints
Authentication

POST /api/auth/signup

POST /api/auth/login

Users

GET /api/users

GET /api/users/:id/roles

POST /api/users/:id/roles

Roles

GET /api/roles

POST /api/roles

PUT /api/roles/:id

DELETE /api/roles/:id

Permissions

GET /api/permissions

POST /api/permissions

PUT /api/permissions/:id

DELETE /api/permissions/:id

Role–Permission

GET /api/roles/:id/permissions

PUT /api/roles/:id/permissions

🔐 Authentication

Protected routes require a JWT token:

Authorization: Bearer <jwt_token>

🚀 Deployment

You can deploy this project on:

Vercel

Render

Railway

Any Node.js hosting platform

📝 License

MIT License