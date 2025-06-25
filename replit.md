# ToonTrivia Throwback - 90s/2000s Cartoon Quiz Game

## Overview

ToonTrivia Throwback is a nostalgic trivia game focusing on 90s and 2000s cartoons. The application features two game modes: Logo Quiz (identify cartoon shows from their logos) and Truth or Lie (spot the false statement among cartoon facts). Built as a full-stack web application with a React frontend and Express backend, it includes scoring systems, leaderboards, and an engaging retro-cartoon aesthetic.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React hooks with custom game state management
- **Styling**: TailwindCSS with custom cartoon-themed design system
- **UI Components**: Radix UI primitives via shadcn/ui components
- **Animations**: Framer Motion for smooth transitions and interactive effects
- **Data Fetching**: TanStack Query (React Query) for server state management

### Backend Architecture
- **Runtime**: Node.js with TypeScript (ES modules)
- **Framework**: Express.js for REST API
- **Development**: tsx for TypeScript execution in development
- **Build System**: esbuild for production bundling

### Data Storage
- **Database**: PostgreSQL (configured via Drizzle ORM)
- **ORM**: Drizzle ORM with Zod schema validation
- **Development Storage**: In-memory storage implementation for rapid development
- **Session Management**: Ready for connect-pg-simple integration

## Key Components

### Game Engine
- **Game State Management**: Custom React hook (`useGameState`) handling scoring, lives, streaks, and question progression
- **Question Types**: Logo identification and Truth/Lie detection games
- **Scoring System**: Point-based with streak bonuses and hint penalties
- **Timer System**: 30-second countdown per question with visual progress indicators

### Data Models
- **Users**: Basic authentication schema ready for implementation
- **Game Scores**: Comprehensive scoring with player names, game modes, and performance metrics
- **Logo Questions**: Show logos with multiple choice answers, hints, and fun facts
- **Truth/Lie Questions**: Three statements with one lie, explanations, and contextual information

### UI/UX Features
- **Responsive Design**: Mobile-first approach with cartoon-inspired visual elements
- **Accessibility**: Full keyboard navigation and screen reader support via Radix UI
- **Visual Feedback**: Animated responses, floating elements, and retro TV screen aesthetics
- **Sound Integration**: Placeholder system for sound effects (ready for audio implementation)

## Data Flow

1. **Game Initialization**: User selects game mode from the main menu
2. **Question Fetching**: API requests random questions based on difficulty and game mode
3. **Answer Processing**: Client validates answers and calculates scores locally
4. **Score Submission**: Final scores are posted to the backend for leaderboard inclusion
5. **Leaderboard Display**: Top scores are fetched and displayed with animations

## External Dependencies

### Development & Build Tools
- **Vite**: Frontend build tool with React plugin and runtime error overlay
- **TypeScript**: Type safety across frontend, backend, and shared schemas
- **PostCSS & Autoprefixer**: CSS processing pipeline

### Database & Validation
- **@neondatabase/serverless**: PostgreSQL serverless driver
- **Drizzle Kit**: Database migrations and schema management
- **Zod**: Runtime type validation and schema generation

### UI & Styling
- **TailwindCSS**: Utility-first CSS framework with custom cartoon color palette
- **Radix UI**: Accessible component primitives
- **Framer Motion**: Animation library for interactive elements
- **Custom Fonts**: Google Fonts integration (Fredoka One, Nunito)

## Deployment Strategy

### Development Environment
- **Platform**: Replit with Node.js 20, PostgreSQL 16 modules
- **Hot Reload**: Vite development server with HMR
- **Database**: Automatic PostgreSQL provisioning via environment variables

### Production Build
- **Frontend**: Vite production build with optimized assets
- **Backend**: esbuild compilation to ESM format
- **Static Assets**: Served from Express with Vite-generated bundle
- **Deployment**: Replit Autoscale with automated build process

### Environment Configuration
- **Development**: `npm run dev` - runs tsx server with Vite middleware
- **Production**: `npm run build && npm run start` - compiled Express server
- **Database**: `npm run db:push` - Drizzle schema migration

## Changelog
- June 22, 2025. Initial setup

## User Preferences

Preferred communication style: Simple, everyday language.