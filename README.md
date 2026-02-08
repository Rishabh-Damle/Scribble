# Scribble

Scribble is a real-time collaborative visual workspace designed for free-form thinking, sketching ideas, and building diagrams directly in the browser.

It enables multiple users to draw, write, and collaborate simultaneously on an infinite canvas with low latency and a smooth, natural drawing experience.

This project focuses on solving real-world challenges around real-time collaboration, synchronization, and scalable system design using modern web technologies.

## Problem Statement

Remote teams, creators, and learners often need a fast and intuitive way to express ideas visually.

Traditional tools can be:

- Heavy or slow to load

- Limited in real-time collaboration

- Overly complex for simple ideation

Scribble aims to provide:

- A lightweight, responsive drawing experience

- Seamless real-time collaboration

- A simple, distraction-free interface for visual thinking

## Core Features

### Interactive Canvas

- Free-hand drawing and shape creation

- Text annotations and basic styling

- Smooth rendering with optimized performance

### Real-Time Collaboration

- Multiple users can join the same workspace

- Instant updates across connected clients

- Low-latency synchronization using WebSockets

### Session-Based Rooms

- Unique drawing rooms

- Users can join and collaborate via shared links

- State synchronization for new participants

### Persistence

- Canvas state stored in the database

- Ability to restore sessions

- Backend-driven state management

### Scalable Architecture

- Real-time events handled via WebSockets

- REST APIs for session and metadata handling

- Clean separation between frontend and backend

## Tech Stack

### Frontend

- Next.js

- React

- TypeScript

- Tailwind CSS

### Backend

- Node.js

- TypeScript

- WebSockets

- HTTP (REST APIs)

### Database & ORM

- PostgreSQL

- Prisma

### Monorepo & Tooling

- Turborepo
- pnpm

### Communication

- WebSockets for real-time updates

- HTTP APIs for session and data management

## Project Structure (High Level)

```
apps/
  web/        # Next.js frontend
  server/     # Backend (WebSockets + APIs)
packages/
  db/         # Prisma schema & client
  shared/     # Shared types and utilities

```

### Frontend (apps/web)

- Canvas rendering logic

- Real-time event listeners

- Tailwind-based UI

- State synchronization with backend

### Backend (apps/server)

- WebSocket server for live collaboration

- REST APIs for rooms and sessions

- Canvas state handling logic

- Event validation and broadcasting

### Database

- Room metadata

- Canvas state snapshots

- Session associations

## Quick Start

### Clone the repository

```
git clone https://github.com/your-username/scribble.git
cd scribble
```

### Install dependencies (Monorepo root)

```
pnpm install

```

### Environment Variables

Create a .env file inside the backend app (apps/server):

```
PORT=5000
DATABASE_URL=your_postgres_connection_string
```

### Run the application

```
pnpm dev

```
