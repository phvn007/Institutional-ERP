# Institutional ERP Platform - Academic Governance & Examination Portal

A comprehensive, full-stack Academic Governance and Result Management ERP system designed for enterprise-level institutional workflows. This platform securely handles grading cycles, student attendance compliance, and result publication across collegiate divisions with strict data integrity.

## ✨ Key Features

*   **Granular Role-Based Access Control (RBAC):** Tailored dashboards and permissions for Super Admins (Principal), Exam Cell Controllers, Department HODs, Faculty, Technical Assistants, and Students.
*   **Optimistic Concurrency Control (OCC):** Prevents race conditions during concurrent grade updates or administrative actions using PostgreSQL row-level locking.
*   **Immutable Audit Ledger:** Tracks every state change and administrative action using a tamper-evident, SHA-256 cryptographic hash chain.
*   **Asynchronous Processing:** Offloads heavy statistical calculations and batch result publishing to distributed Celery workers via Redis.
*   **Embedded Analytics:** Generates server-side statistical summaries and bell-curve distribution visualizations using Pandas and Seaborn.
*   **Dual-Key Security:** Enforces strict executive clearance (e.g., emergency result rollbacks) requiring statutory authorization.

## 💻 Technology Stack

**Frontend**
*   **Core:** React 19, TypeScript, Vite
*   **Styling & UI:** Tailwind CSS v4, Motion (animations), Lucide React
*   **Architecture:** Finite State Machine logic for state transitions

**Backend**
*   **Framework:** FastAPI (Python 3)
*   **Database:** PostgreSQL 16 with SQLAlchemy 2.0 & Alembic
*   **Async Workflows:** Celery, Redis 7
*   **Data Science:** Pandas, NumPy, Seaborn, Matplotlib
*   **Security:** JWT authentication, Bcrypt hashing

**Infrastructure**
*   **Containerization:** Docker & Docker Compose
*   **Web Server:** Nginx (Frontend serving)

for installing node modules npm install
to run the server npm run dev
