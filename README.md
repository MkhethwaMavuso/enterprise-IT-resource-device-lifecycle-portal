# enterprise-IT-resource-device-lifecycle-portal
A high-performance, enterprise-grade hardware and software lifecycle management platform engineered for real-time asset provisioning, automated maintenance scheduling, immutable audit trails, and end-to-end device retirement workflows using Next.js 15, TypeScript, Express.js, Prisma ORM, and PostgreSQL.

🚀 DevicePulse — Enterprise IT Resource & Device Lifecycle Portal

A high-performance, enterprise-grade hardware and software lifecycle management platform engineered for real-time asset provisioning, automated maintenance scheduling, immutable audit trails, and end-to-end device retirement workflows using Next.js 15, TypeScript, Express.js, Prisma ORM, and PostgreSQL.

🎯 1. The Problem Statement

The Core Pain Point: Enterprise IT operations and asset management teams frequently face unrecorded device allocations, ghost hardware, untracked warranty expirations, and missing security compliance records during offboarding.

The Business Impact: Unmonitored IT assets lead to severe compliance risks, unnecessary procurement expenditures, hardware theft, and expensive administrative overhead during annual software/hardware audits.

The Target Persona: Built for Enterprise IT Directors, System Administrators, Asset Logistics Specialists, and Security Operations Leads.

💡 2. The Solution Statement

The Technical Approach: DevicePulse delivers a centralized IT lifecycle management hub featuring automated asset status transitions (PROCURED ➔ PROVISIONED ➔ MAINTENANCE ➔ DECOMMISSIONED), Prisma ORM relational validation, server-side data fetching via Next.js App Router, and strict role-based access control.

Core Value Proposition: Real-time asset lifecycle tracking, automated warranty alert triggers, zero-latency audit logs, and optimized relational database queries designed for thousands of managed endpoints.

🛠️ 3. Tech Stack & Architecture

Frontend: Next.js 15 (App Router, Server Actions, React Server Components) / React 18 / TypeScript / Tailwind CSS / Shadcn UI / Lucide Icons

Backend & API: Node.js / Express.js REST APIs / Zod Schema Validation / RESTful Asset Lifecycle Controllers

Database & Persistence: PostgreSQL / Prisma ORM / Relational 3NF Schema (Device, Assignment, MaintenanceLog, User)

Security & Auth: NextAuth.js / JWT (JSON Web Tokens) / bcrypt password hashing / CORS Policy Enforcement / RBAC Middleware

Infrastructure & Tooling: Vercel Edge Deployment / Render / Docker Containerization / Git & GitHub CI/CD Pipelines

🗺️ 4. System Architecture & Logical Flow

High-Level Pipeline

Client UI (Next.js IT Command Center & Portal)
       │
       ▼
Auth Middleware & RBAC Interceptor (JWT Claims & Role Checking)
       │
       ▼
Express.js REST Controllers & Next.js Server Actions (Lifecycle Engine)
       │
       ▼
Prisma ORM (Relational Consistency & Lifecycle State Validation)
       │
       ▼
PostgreSQL Database (Normalized 3NF Persistent Storage)


Logical User Flow

Authentication: Users authenticate securely; NextAuth issues a signed JWT containing embedded role claims (IT_ADMIN, ASSET_MANAGER, EMPLOYEE).

Authorization: Middleware intercepts incoming API and Server Action calls, verifying RBAC permissions before granting lifecycle mutation access.

Execution: Validated requests update device states, automatically create immutable MaintenanceLog or Assignment records, and return structured JSON responses to the client UI.

🌟 5. Key Features & Capabilities

🔒 Granular RBAC: Multi-tiered role permissions restricting device provisioning, reassignment, and decommissioning rights to authorized IT staff.

⚡ Real-Time Lifecycle Tracking: Complete visibility into device health, custody transfers, physical locations, and upcoming maintenance schedules.

🛡️ Secure Endpoints: Protected against SQL injection via Prisma query parameterization, XSS attacks, and unauthenticated API calls.

📊 Optimized 3NF Schemas: Fully normalized database tables indexed for rapid filtering across serial numbers, MAC addresses, and assignment histories.

⚙️ 6. Getting Started Locally (Quickstart)

Prerequisites

Node.js 18.x or higher installed locally.

A running PostgreSQL database instance.

Installation Steps

Clone the Repository:

git clone https://github.com/YourUsername/devicepulse-it-lifecycle.git
cd devicepulse-it-lifecycle


Install Dependencies:

npm install


Configure Environment Variables:
Create a .env file in the root directory and add your credentials:

DATABASE_URL="postgresql://user:password@localhost:5432/devicepulse_db?schema=public"
JWT_SECRET="your_cryptographic_jwt_secret_key"
NEXTAUTH_SECRET="your_nextauth_secret"
NEXTAUTH_URL="http://localhost:3000"
PORT=5000


Run Database Migrations:

npx prisma db push


Start Development Server:

npm run dev


Open http://localhost:3000 to access the DevicePulse IT Resource Portal.

📄 License

Distributed under the MIT License. See LICENSE for details.

Author: Developed by Mkhethwa Mavuso — Full-Stack Architect & Enterprise Systems Engineer.
