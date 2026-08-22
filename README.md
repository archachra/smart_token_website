# SmartToken Team Website

This repository contains the team website for the SmartToken software engineering project.

The site is a React frontend for the project presentation and documentation, with a local Node.js + Express backend for admin workflow support.

## What the website includes

- Public homepage with the SmartToken project overview
- Team page with finalized members and responsibilities
- Project page describing the approved SmartToken problem and system idea
- Presentations area for the planning presentation and later deliverables
- Admin page for local login, deliverable/version management, file upload, and publish actions

## What SmartToken is

SmartToken is the approved university project for a low-interruption, faculty-controlled participation/token system in live university labs.

It is not a document-management product or a generic points tracker.

## Local development

Frontend:

```bash
npm install
npm run dev
```

Backend:

```bash
cd server
npm install
npm start
```

The frontend runs on Vite, and the backend runs on `http://localhost:3001`.

## Backend environment

The backend reads configuration from `server/.env`:

```env
PORT=3001
DB_HOST=localhost
DB_PORT=5432
DB_NAME=smarttoken
DB_USER=postgres
DB_PASSWORD=your_password
JWT_SECRET=replace_with_a_long_random_secret
JWT_EXPIRES_IN=1d
```

Use `server/.env.example` as the template.

## Current backend features

- `GET /api/health`
- `GET /api/db-health`
- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/deliverables`
- `GET /api/deliverables/:id`
- `GET /api/deliverables/:id/versions`
- `POST /api/deliverables`
- `POST /api/versions`
- `PATCH /api/versions/:id/publish`
- `POST /api/files/upload`

## Notes

- The planning presentation is embedded directly in the website.
- The admin workflow uses the existing backend APIs and JWT session storage.
