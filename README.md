# Excelidraw

Excelidraw is a modern, real-time collaborative whiteboard application. I built this project to enable multiple users to draw, sketch, and collaborate on a shared infinite canvas simultaneously. The application features room-based sessions, seamless real-time updates via WebSockets, and user authentication, all structured within a highly scalable monorepo architecture.

## Features

* **Real-Time Collaboration:** Instant synchronization of drawings and canvas updates across multiple clients.
* **Room-Based Sessions:** Create isolated rooms for different teams or projects.
* **Infinite Canvas:** Unrestricted drawing space with panning and zooming capabilities.
* **User Authentication:** Secure sign-up and sign-in functionality.
* **Scalable Architecture:** Monorepo setup utilizing Turborepo for optimized build times and shared packages.

## Tech Stack

* **Frontend:** Next.js 15, React, TypeScript, Tailwind CSS
* **Backend:** Node.js, Express.js
* **Real-Time Engine:** WebSockets (`ws`)
* **Database & ORM:** PostgreSQL, Prisma ORM
* **Monorepo Tooling:** Turborepo, pnpm

## Project Structure

This project uses Turborepo to manage multiple applications and shared packages.

### Apps

* `apps/excelidraw-frontend`: The main Next.js web application encompassing the canvas interface and user routing.
* `apps/http-backend`: The Express server handling REST API requests, user authentication, and room management.
* `apps/ws-backend`: The dedicated WebSocket server responsible for broadcasting real-time drawing events to connected clients.
* `apps/web`: Secondary web application or landing page module.

### Packages

* `packages/db`: Prisma database schema, migrations, and the generated Prisma client.
* `packages/ui`: Shared React components used across the frontend applications.
* `packages/common`: Shared TypeScript types, validation schemas, and constants.
* `packages/backend-common`: Shared utility functions and configurations for the Node.js backends.
* `packages/eslint-config`: Shared ESLint configurations.
* `packages/typescript-config`: Shared `tsconfig.json` configurations.

## Getting Started

Follow these steps to set up the project locally.

### Prerequisites

* Node.js (v18 or higher)
* pnpm 
* PostgreSQL database

### Installation

Clone the repository:

```bash
git clone [https://github.com/your-username/real-time-collaborative-whiteboard.git](https://github.com/your-username/real-time-collaborative-whiteboard.git)
cd real-time-collaborative-whiteboard
