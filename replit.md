# DogeRAT

## Overview

DogeRAT is a Node.js application that appears to be a remote administration tool (RAT) with Telegram bot integration. The application uses Express.js as its web server, WebSocket for real-time communication, and integrates with the Telegram Bot API for command and control functionality. It includes file upload capabilities via Multer and HTTP request handling through Axios.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Backend Framework
- **Express.js** serves as the primary web server framework
- **WebSocket (ws)** provides real-time bidirectional communication between the server and connected clients
- **Body-parser** handles JSON and URL-encoded request parsing

### Communication Layer
- **Telegram Bot API Integration**: Uses `node-telegram-bot-api` for receiving commands and sending responses through Telegram
- **WebSocket Server**: Enables persistent connections for real-time data exchange with clients
- **Axios**: Handles outbound HTTP requests to external services

### File Handling
- **Multer**: Manages file uploads with multipart/form-data support

### Identification System
- **UUID**: Generates unique identifiers, likely for tracking connected clients or sessions

### Entry Point
- Main application logic resides in `index.js`
- Application starts via `npm start` which runs `node index.js`

### Runtime Environment
- Targets Node.js version 16.13.2 specifically

## External Dependencies

| Dependency | Purpose |
|------------|---------|
| `express` | Web server framework |
| `ws` | WebSocket server for real-time communication |
| `node-telegram-bot-api` | Telegram bot integration for C2 communication |
| `axios` | HTTP client for external API requests |
| `multer` | File upload handling |
| `body-parser` | Request body parsing middleware |
| `uuid` | Unique identifier generation |

### Required Configuration
- **Telegram Bot Token**: Required for bot functionality (likely configured in index.js or environment variables)
- **Port Configuration**: Express server port needs to be defined
- **WebSocket Configuration**: WS server setup required for client connections