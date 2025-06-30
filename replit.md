# Period Tracker Application

## Overview

This is a React-based period tracking application with a Node.js/Express backend. The application allows users to track menstrual cycle data including flow type, mood, fatigue, skin condition, weight, and personal comments. Data is stored in Notion via API integration, with authentication handled through a simple access code system.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Framework**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React hooks with TanStack Query for server state
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Storage**: PostgreSQL sessions with connect-pg-simple
- **Development**: Hot reload with tsx and Vite middleware integration

### Authentication
- Simple access code-based authentication
- No traditional user registration/login system
- Access controlled through environment variable configuration

## Key Components

### Database Schema
- **Users Table**: Basic user management with username/password fields
- **Database Configuration**: PostgreSQL with Drizzle ORM migrations
- **Connection**: Neon Database serverless PostgreSQL instance

### External Integrations
- **Notion API**: Primary data storage for period tracking entries
- **Environment Variables**: 
  - `VITE_ACCESS_CODE`: Authentication access code
  - `VITE_NOTION_API_KEY`: Notion API authentication
  - `VITE_DATABASE_ID`: Target Notion database ID
  - `DATABASE_URL`: PostgreSQL connection string

### UI Components
- Comprehensive component library using shadcn/ui
- Responsive design with mobile-first approach
- Dark/light theme support through CSS variables
- Form components with validation and error handling

## Data Flow

1. **User Authentication**: Access code verification against environment variable
2. **Data Collection**: Form-based data entry for period tracking metrics
3. **Data Validation**: Client-side validation using React Hook Form and Zod
4. **External Storage**: Direct API calls to Notion for data persistence
5. **Local Storage**: In-memory storage implementation for development/testing

## External Dependencies

### Core Dependencies
- **React Ecosystem**: React, React DOM, React Router (Wouter)
- **UI Framework**: Radix UI primitives, Lucide React icons
- **Backend**: Express.js, Drizzle ORM, Neon Database client
- **Development**: Vite, TypeScript, ESBuild for production builds
- **Styling**: Tailwind CSS, PostCSS, Autoprefixer

### Third-Party Services
- **Notion API**: External data storage and management
- **Neon Database**: Serverless PostgreSQL hosting
- **Replit Integration**: Development environment optimizations

## Deployment Strategy

### Development Environment
- **Local Development**: `npm run dev` with hot reload
- **Database Management**: `npm run db:push` for schema synchronization
- **Type Checking**: `npm run check` for TypeScript validation

### Production Build
- **Frontend**: Vite build process generating optimized static assets
- **Backend**: ESBuild bundling for Node.js deployment
- **Static Assets**: Served from `dist/public` directory
- **Server**: Express server serving both API and static files

### Architecture Decisions

**Frontend Framework Choice**: React with TypeScript chosen for type safety and ecosystem maturity. Vite selected over Create React App for faster development experience and better build optimization.

**UI Component Strategy**: shadcn/ui provides consistent, accessible components while maintaining customization flexibility. Radix UI primitives ensure accessibility compliance.

**Backend Simplicity**: Express.js chosen for straightforward API development. Minimal server-side logic with primary data storage handled by external Notion API.

**Database Strategy**: Dual approach with PostgreSQL for potential user management and Notion API for primary data storage. This allows for future expansion while maintaining current simplicity.

**Authentication Approach**: Simple access code system chosen over complex user management for privacy and ease of use in personal tracking application.

## Changelog

- June 30, 2025. Initial setup
- June 30, 2025. Added settings/admin panel for managing API keys and login credentials
- June 30, 2025. Implemented dynamic configuration system with file-based storage
- June 30, 2025. Updated Notion integration to use changeable credentials
- June 30, 2025. Deployed application with full functionality

## User Preferences

Preferred communication style: Simple, everyday language.