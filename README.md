# MythicHeats – University Submission
## Team Members :
Ahmed Nazim (24L-2611)
Ahmad Khan (24L-2541)
## Project Structure
/backend: Contains Supabase configuration, Edge Functions, and application logic.
/frontend: Contains the React source code, components, and frontend dependencies.
/database: Contains schema.sql (DDL statements) .
/docs: Contains Iteration_1.docx and the project report.docx.

## Description
MythicHeats is a specialized academic management and resource platform designed for FAST-NUCES students. The system features secure Google OAuth restricted to university domains, automated roll-number-based username generation, and integrated resource management using a modern web stack.


> **Note for TA:** The root directory serves as the **Frontend** folder for deployment purposes.
> The React app runs directly from the project root. Please `cd .` (stay in root) to run the frontend.

## How to Run the Frontend

```sh
# 1. Install dependencies
npm install

# 2. Start the development server
npm run dev
```

The app will be available at `http://localhost:5173`.

## Tech Stack

| Layer      | Technology                          |
|------------|-------------------------------------|
| Frontend   | React, TypeScript, Vite, Tailwind CSS, shadcn/ui |
| Backend    | Supabase (Edge Functions, Auth, RLS) |
| Database   | PostgreSQL (hosted via Supabase)     |
| Auth       | Google OAuth (restricted to @lhr.nu.edu.pk) |

## Backend

The `backend/supabase/` folder contains:
- **Edge Functions** – Serverless functions (e.g., Google Sheets sync)
- **Migrations** – SQL migration files for database schema changes
- **config.toml** – Supabase project configuration

## Database

The `database/schema.sql` file contains the complete database schema including:
- All table definitions (usernames, chat_messages, courses, notifications, google_sheets_data)
- Row-Level Security (RLS) policies for each table

## Authentication

- Google OAuth login restricted to `@lhr.nu.edu.pk` domain
- Admin bypass for designated owner email
- Auto-generated usernames from Google metadata + roll number

## Live Deployment
-It is still in process due to issue in availability of domain
- **URL:** https://mythicheats.lovable.app
