# AI Tennis Coach

## Overview

The AI Tennis Coach is a full-stack web application that provides automated tennis technique analysis using AI-powered video processing. Users can upload videos of their tennis shots (serves, forehands, backhands, volleys, and slices) and receive detailed feedback on their technique, including summaries, analysis, and improvement tips. The application uses Google's Gemini API for video analysis and provides structured markdown feedback to help players improve their game.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18+ with TypeScript
- **Build Tool**: Vite for fast development and optimized production builds
- **Styling**: Custom CSS with modern design patterns, gradients, and responsive layouts
- **File Handling**: HTML5 file input for video uploads with client-side validation
- **State Management**: React hooks (useState) for local component state
- **UI Components**: Custom form components for shot type selection and file uploads

### Backend Architecture
- **Framework**: Express.js with TypeScript support
- **API Design**: RESTful endpoints with `/api/analyze` for video processing
- **File Upload**: Multer middleware for handling multipart form data and video files
- **Static Serving**: Express static middleware to serve the built React application
- **Error Handling**: Basic error responses with HTTP status codes

### Data Processing
- **AI Integration**: Google Gemini API for video analysis and technique feedback
- **Video Processing**: Base64 encoding for video data transmission to Gemini
- **Response Processing**: Custom markdown formatting and prettification for structured feedback
- **File Storage**: Temporary local storage for uploaded videos during processing

### Development Setup
- **Monorepo Structure**: Separate client and server directories with shared build processes
- **Concurrent Development**: Uses concurrently to run both frontend and backend during development
- **Path Aliases**: TypeScript path mapping for clean imports (@/, @shared/)
- **Build Process**: Separate build commands for client (Vite) and server (esbuild)

## External Dependencies

### AI and Media Processing
- **Google Gemini API**: Primary AI service for video analysis and tennis technique feedback
- **Multer**: File upload handling and temporary storage
- **node-fetch**: HTTP client for API communication with external services

### Frontend Libraries
- **React & React-DOM**: Core UI framework (v18+)
- **Vite**: Build tool and development server
- **TypeScript**: Type safety and development tooling

### Backend Services
- **Express.js**: Web server framework
- **CORS**: Cross-origin resource sharing middleware
- **Node.js File System**: Local file operations for video processing

### Development Tools
- **Concurrently**: Parallel process execution for development
- **ESLint**: Code linting and quality assurance
- **TypeScript Compiler**: Type checking and compilation

### Notable Integrations
- **Replit-specific plugins**: Runtime error overlay and cartographer for Replit deployment
- **Static Asset Serving**: Direct serving of uploaded files through Express static middleware
- **Environment-aware Configuration**: Different build and development configurations based on NODE_ENV