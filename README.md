# AppsDev API

A TypeScript and Express.js API starter for AppsDev students. This project provides a layered folder structure (`config`, `controllers`, `services`, `repositories`, `routes`, `middlewares`, `schema`, `lib`, `utils`) ready for building REST API features on top of it.

## Prerequisites

- Node.js LTS (v20+ recommended)
- npm

## Getting started

```bash
# 1. Install dependencies
npm install

# 2. Create your environment file from the example (PowerShell)
Copy-Item .env.example .env

# 3. Start the development server
npm run dev
```

The API runs at `http://localhost:7000` by default.

## Test the API

In Postman (or your browser), send a `GET` request to:

```
http://localhost:7000/api/health
```

Expected response:

```json
{
  "status": "success",
  "message": "API is healthy",
  "timestamp": "2026-09-18T00:00:00.000Z"
}
```

## Useful commands

```bash
npm run dev        # start the dev server with auto-restart
npm run lint       # run ESLint
npm run build      # bundle the production build into dist/
npm start          # run the production build
npm run db:generate  # generate the Prisma client (requires a database)
npm run db:migrate   # apply Prisma migrations (requires a database)
npm run contract:emit  # emit the Prisma contract types
```

## Project structure

```
src/
├── config/        # Environment configuration
├── controllers/   # Request handlers
├── lib/           # Shared integrations and helpers
├── middlewares/   # Express middleware
├── repositories/  # Database access
├── routes/        # Route definitions
├── schema/        # Validation schemas
├── services/      # Application business logic
└── utils/         # Small reusable utilities
```

## Environment variables

See `.env.example` for the full list. Never commit `.env` to version control; it may contain real credentials.