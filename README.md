# Student Achievement Management System (SAMS)

A centralized, role-based platform for managing, verifying, and tracking student achievements at GGSIP University.

**Live Demo:** https://bpit-portal.vercel.app/

## Overview

The Student Achievement Management System (SAMS) streamlines the process of recording, reviewing, verifying, and reporting student achievements. It provides dedicated workflows for Students, Mentors, and Heads of Department (HODs), reducing manual administrative work and improving transparency across the achievement verification lifecycle.

Designed to support 500+ students annually, the system organizes achievement records, proof documents, approval workflows, mentor allocations, and administrative reports in one platform.

## Key Features

### Role-Based Access Control
- Three roles: Student, Mentor, and HOD.
- Role-scoped access to relevant records and actions.
- Structured workflows for achievement submission, review, and approval.

### Student Achievement Management
- Manage extracurricular and co-curricular achievements.
- Maintain project, research, and other academic achievement records.
- Upload supporting documents as proof of achievements.

### Mentor Verification Workflow
- Route student achievement submissions to the assigned mentor for verification.
- Review supporting proof documents.
- Track achievement approval status through the verification process.

### HOD Administration
- Assign and reassign mentors to students.
- Manage approval overrides and administrative workflows.
- Access student-, class-, and batch-wise reports.
- Export achievement data to Excel for reporting and analysis.

### Document Management
- Cloudinary integration for proof document uploads and storage.
- Centralized access to supporting achievement documents.

### Auditability and Data Management
- Prisma ORM for structured database access.
- Database schema designed to support approval audit trails.
- MySQL for persistent application data.

## Tech Stack

| Technology | Purpose |
|---|---|
| Next.js | Full-stack web application framework |
| React | Component-based user interface |
| Tailwind CSS | Responsive UI styling |
| MySQL | Relational database |
| Prisma ORM | Database schema, queries, and data access |
| Cloudinary | Achievement proof document management |
| Vercel | Frontend/application deployment |
| Amazon Web Services (AWS) | Backend deployment |
| Git and GitHub | Version control and collaboration |

## System Architecture

The application uses a web frontend, server-side application logic, and a relational database, with Cloudinary handling uploaded proof documents.

```text
                 Students / Mentors / HOD
                           |
                           v
                    Next.js Application
                    (Vercel Deployment)
                           |
                  Server-side Logic / APIs
                           |
                  +--------+--------+
                  |                 |
                  v                 v
              Prisma ORM        Cloudinary
                  |
                  v
                MySQL
          (Relational Database)
```

The backend deployment and API configuration should reflect the actual production setup. AWS is used for the backend deployment as configured for this project.

## Workflow

1. **Student submission:** Students submit achievement records with supporting proof documents.
2. **Document upload:** Supporting documents are uploaded through Cloudinary integration.
3. **Mentor verification:** The assigned mentor reviews the submitted achievement and its supporting evidence.
4. **Administrative oversight:** HODs manage mentor allocations and applicable approval overrides.
5. **Reporting:** Authorized administrators generate student-, class-, and batch-wise reports and export data to Excel.

## Getting Started

### Prerequisites

- Node.js and npm
- MySQL
- Git
- A Cloudinary account
- The required environment variables for the application

### 1. Clone the repository

```bash
git clone https://github.com/Janitberwal/SAMS-.git
cd BPIT_Portal
```

If the repository URL or directory name differs, replace it with the correct value.

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root and configure the variables required by your implementation.

Example:

```env
DATABASE_URL="mysql://USER:PASSWORD@HOST:3306/DATABASE_NAME"
CLOUDINARY_CLOUD_NAME="your_cloud_name"
CLOUDINARY_API_KEY="your_api_key"
CLOUDINARY_API_SECRET="your_api_secret"
```

Use the exact variable names expected by your application. Never commit real credentials, API secrets, or production environment files to GitHub.

### 4. Set up Prisma

If the project uses Prisma migrations, apply the existing migrations:

```bash
npx prisma migrate deploy
```

Generate the Prisma Client if required:

```bash
npx prisma generate
```

Use the migration commands appropriate to your existing schema and deployment setup.

### 5. Start the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Deployment

- **Live Application:** [bpit-portal.vercel.app](https://bpit-portal.vercel.app/)
- **Frontend / Next.js Application:** Vercel
- **Backend Infrastructure:** Amazon Web Services (AWS)
- **Database:** MySQL
- **Document Storage:** Cloudinary

Ensure production environment variables, database connectivity, and Cloudinary credentials are configured securely in the relevant deployment environments.

## Project Impact

- Designed to support 500+ students annually.
- Supports a 1:30 mentor-to-student allocation ratio.
- Centralizes achievement submissions and supporting documentation.
- Streamlines mentor verification and HOD-level administration.
- Enables multi-level Excel reporting for administrative tracking.

## Future Enhancements

Potential improvements include automated testing, enhanced analytics dashboards, notification workflows, and expanded monitoring and audit capabilities.

## Author

**Janit Berwal**

- GitHub: [@Janitberwal](https://github.com/Janitberwal)
- Project: [Student Achievement Management System](https://bpit-portal.vercel.app/)

---

Built to simplify student achievement management through structured workflows, role-based access, and centralized reporting.
