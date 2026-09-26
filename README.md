# 🏥 MediDesk — Modern Dental & Clinic Management Platform

[![Next.js](https://img.shields.io/badge/Frontend-Next.js%2016-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![Node.js](https://img.shields.io/badge/Backend-Node.js%20%2F%20Express-339933?style=flat-square&logo=node.js)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/Language-TypeScript-3178C6?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb)](https://www.mongodb.com/)
[![Tailwind CSS](https://img.shields.io/badge/Styling-Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss)](https://tailwindcss.com/)

MediDesk is a comprehensive, multi-tenant clinic management SaaS platform engineered specifically for dental practices and healthcare clinics. It streamlines clinical workflows, patient record keeping, medical imaging management (X-Rays/Scans), staff invitations with Role-Based Access Control (RBAC), and appointment scheduling.

---

## 🔗 Live Demo & Repositories

- Live Demo :\*\* [MediDesk Live Demo](https://medi-desk-frontend.vercel.app/)

---

The platform is architected into a client-server structure. You can navigate directly to the individual repositories below:

- ** Frontend Repository (App Router):** [MediDesk Client Repo](https://github.com/MAldeep/mediDesk_frontend)
- ** Backend Repository (RESTful API):** [MediDesk Server Repo](https://github.com/MAldeep/MediDesk_Backend)

---

## ✨ Key Features

### 👨‍⚕️ Patient Management System

- Full CRUD operations for patient records with advanced search, dynamic pagination, and sorting.
- Comprehensive patient profile views including medical history, personal details, and clinical notes.

### 🖼️ Scans & Medical Radiology (Cloudinary Integration)

- Dynamic medical scan uploads (X-Rays, Lab Reports) with real-time file preview.
- High-resolution Lightbox viewer for detailed scan inspection.
- Secure image deletion syncing Cloudinary assets with MongoDB arrays ($pull).

🛡️ Role-Based Access Control (RBAC) & Team Management

- Multi-tier authorization matrix (**Admin**, **Doctor**, **Staff/Assistant**).
- Dynamic User Invitation System with secure email/token assignment.
- Granular permission hooks enforcing strict access control on sensitive clinical operations.

📅 Comprehensive Appointment Scheduling System

End-to-end appointment lifecycle management (Scheduled, Completed, Cancelled).

Real-time appointment creation, status tracking, and automated schedule conflict prevention.

Dynamic filtering by date, practitioner, and patient status to streamline daily clinic operations.

---

## 🛠️ Tech Stack & Architecture

### **Frontend**

- **Framework:** Next.js 16 (App Router with React Server/Client Components)
- **State Management & Data Fetching:** TanStack Query v5 (React Query)
- **Forms & Validation:** React Hook Form + Zod
- **Styling & UI:** Tailwind CSS, Lucide Icons, Framer Motion
- **HTTP Client:** Axios with custom interceptors for Token refresh & Error handling

### **Backend**

- **Runtime & Framework:** Node.js, Express.js (TypeScript)
- **Database & ORM:** MongoDB with Mongoose Schema validation
- **Cloud Storage:** Cloudinary API (Stream Uploads & Asset destruction)
- **Authentication:** JWT (JSON Web Tokens) with Refresh Token flow & Bcrypt hashing

---

## 📂 Project Structure

```text
medidesk/ (Parent / Workspace)
 ├── 📁 medidesk-client/      # Next.js Frontend Application
 │    ├── app/
 │    │    ├── components/    # Reusable UI Components & Sections
 │    │    ├── hooks/         # Custom React Query & RBAC Hooks
 │    │    ├── services/      # Axios API Client & Endpoint Handlers
 │    │    └── dashboard/     # Role-based App Router Routes
 │    └── public/
 │
 ├── 📁 medidesk-server/      # Express.js REST API
 │    ├── src/
 │    │    ├── controllers/   # Request Handlers & Business Logic
 │    │    ├── models/        # Mongoose Schemas & TypeScript Interfaces
 │    │    ├── routes/        # API Endpoints Router
 │    │    ├── services/      # Core Services (Cloudinary, DB Operations)
 │    │    └── middlewares/   # Auth, RBAC, and Error Handlers
 │
 └── README.md                # Parent Repository Documentation
```
