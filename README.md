## 🔐 RBAC Admin Dashboard

Enterprise-grade Role-Based Access Control system with advanced security, audit logging, and multi-tenancy support

🎯 Live Demo
Try it now: https://rbac-tool-igdr.vercel.app/signin
Test Credentials:

Email: aditi@gmail.com
Password: aditi123


🌟 Overview
A production-ready RBAC Admin Dashboard built for modern SaaS applications requiring sophisticated access control. This system goes beyond basic role management by implementing hierarchical permissions, audit trails, session management, and real-time security monitoring.

## 📚 What is RBAC?

**RBAC (Role-Based Access Control)** is an authorization model that defines:

- **Users** → people using the system  
- **Roles** → collections of permissions (Admin, Editor, Viewer)  
- **Permissions** → specific allowed actions (create, update, delete, view)

Instead of assigning permissions directly to each user, users are assigned roles, and roles determine what actions are allowed.  
This makes the system **secure, maintainable, and scalable**.

---

## 🚀 Features

- JWT-based authentication  
- Secure password hashing with bcrypt  
- User management  
- Role management  
- Permission management  
- Role–Permission assignment  
- User–Role assignment  
- Protected API routes using middleware  
- RESTful API architecture  

---

## 🛠️ Tech Stack 

**Frontend & Backend**
- Next.js (App Router)
- TypeScript
- Tailwind CSS
- shadcn/ui  

### Database
- PostgreSQL  
- Prisma ORM  

### Authentication & Security
- JSON Web Tokens (JWT)  
- bcrypt  

### Tooling
- Prisma Migrate  
- dotenv  
- Nodemon  

---

## 📁 Project Structure (Next.js App Router)

```txt
app/
├── api/                 # Backend API routes
│   ├── auth/            # Authentication APIs
│   ├── roles/           # Role APIs
│   ├── permissions/     # Permission APIs
│   └── users/           # User-role APIs
│
├── dashboard/           # Admin dashboard pages
├── roles/               # Roles management UI
├── permissions/         # Permissions management UI
├── role-permissions/    # Role–permission assignment UI
├── signin/              # Login page
├── signup/              # Signup page
│
├── components/          # Reusable UI & layout components
│   ├── layout/          # Dashboard layout & sidebar
│   └── ui/              # shadcn/ui components
│
├── store/               # Global RBAC state
├── hooks/               # Custom React hooks
├── lib/                 # Prisma client & utilities
│
├── layout.tsx           # Root layout
├── page.tsx             # Landing page
├── globals.css          # Global styles
│
middleware.ts            # Route protection (JWT)
prisma/
└── schema.prisma        # Database schema
```

---

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/rbac_db
JWT_SECRET=your-secret-key
JWT_EXPIRES_IN=24h

```
## ▶️ Run Locally

```bash
npm install
npx prisma migrate dev
npm run dev

```

## 🧪 Testing

```
Sample test credentials (after signup):

Email: test@example.com
Password: test1234

```

## 📝 License
```
This project is licensed under the MIT License.
```
