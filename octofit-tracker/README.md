# Octofit Tracker - Multi-Tier Application

A modern multi-tier application for fitness tracking with React 19 frontend and Node.js/Express backend.

## Architecture

### Frontend
- **Framework**: React 19
- **Build Tool**: Vite
- **Port**: 5173
- **Location**: `./frontend`

### Backend
- **Runtime**: Node.js
- **Framework**: Express
- **Language**: TypeScript
- **Port**: 8000
- **Location**: `./backend`

### Database
- **System**: MongoDB
- **Port**: 27017
- **ODM**: Mongoose

## Project Structure

```
octofit-tracker/
├── frontend/                 # React 19 + Vite application
│   ├── src/
│   ├── public/
│   ├── vite.config.js
│   ├── package.json
│   └── .env
├── backend/                  # Express + TypeScript API server
│   ├── src/
│   │   └── server.ts        # Main server entry point
│   ├── dist/                # Compiled JavaScript (after build)
│   ├── tsconfig.json
│   ├── package.json
│   └── .env
└── README.md
```

## Setup Instructions

### Prerequisites
- Node.js (v18+)
- npm or yarn
- MongoDB running locally (or configure MONGODB_URI)

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Access at: `http://localhost:5173`

### Backend Setup

```bash
cd backend
npm install
npm run dev
```

Server running at: `http://localhost:8000`

### Database Setup

Ensure MongoDB is running on port 27017:

```bash
# Using Docker (optional)
docker run -d -p 27017:27017 --name mongodb mongo
```

## Environment Variables

### Frontend (`.env`)
```
VITE_API_URL=http://localhost:8000
VITE_APP_NAME=Octofit Tracker
```

### Backend (`.env`)
```
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
NODE_ENV=development
```

## Available Scripts

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

### Backend
- `npm run dev` - Start development server with ts-node
- `npm run build` - Compile TypeScript to JavaScript
- `npm start` - Run compiled JavaScript

## API Endpoints

- `GET /` - Welcome message and version
- `GET /api/health` - Health check endpoint

## Technology Stack

- **Frontend**: React 19, Vite, TypeScript (optional)
- **Backend**: Express 5, TypeScript, Mongoose 9
- **Database**: MongoDB
- **Package Manager**: npm

## Development Workflow

1. Start MongoDB: `docker run -d -p 27017:27017 mongo`
2. Start Backend: `cd backend && npm run dev`
3. Start Frontend: `cd frontend && npm run dev`
4. Open browser to `http://localhost:5173`

## Build for Production

### Frontend
```bash
cd frontend
npm run build
npm run preview
```

### Backend
```bash
cd backend
npm run build
npm start
```

## License

ISC
