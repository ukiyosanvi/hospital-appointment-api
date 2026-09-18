# Hospital Appointment API

A CRUD module for a hospital appointment system built with Prisma 7 and PostgreSQL.

## Overview

This project introspects an existing PostgreSQL database (`patients`, `doctors`, `appointments` tables) using `prisma db pull`, cleans the generated schema to follow Prisma conventions (PascalCase models, camelCase fields, `@map`/`@@map`), and implements full CRUD operations for all three models.

## Features

- **Patient CRUD**: create, read, search, update, delete
- **Doctor CRUD**: create, read, list by specialty, delete
- **Appointment relations**: booking via `connect`, fetching nested data via `include`
- Database seeding with `prisma db seed`
- End-to-end test script exercising every operation

## Setup

1. Install dependencies: `npm install`
2. Set `DATABASE_URL` in `.env`
3. Run `npx prisma generate`
4. Seed the database: `npx prisma db seed`
5. Run the test script: `npx tsx src/test.ts`

## Tech Stack

- Prisma 7 with the PostgreSQL driver adapter (`@prisma/adapter-pg`)
- TypeScript
- tsx for running seed/test scripts
