# Anonymous Messaging Platform (NGL-like)

## Overview
A web application similar to NGL where people can send anonymous messages. Users can ask questions anonymously without revealing their identity, and the admin can view all messages and reply to them through an admin interface.

## Project Goals
- Anonymous messaging system where users can send messages without revealing their identity
- Admin interface to view all conversations and reply to messages  
- Users can only see their own conversation thread with admin replies
- Deployable on Railway.app platform

## Current State
✅ Fully functional anonymous messaging platform
- Frontend and backend implemented
- Database schema created and initialized
- Admin dashboard working
- Session-based conversation tracking
- Ready for Railway deployment

## Recent Changes
- **2025-09-03**: Created complete anonymous messaging platform
  - Set up Express.js server with Handlebars templating
  - Implemented PostgreSQL database with conversations and messages tables
  - Created anonymous messaging interface for users
  - Built admin dashboard for viewing and replying to messages
  - Added session management for conversation tracking
  - Configured Railway deployment settings

## Project Architecture

### Technology Stack
- **Backend**: Node.js with Express.js
- **Database**: PostgreSQL with native pg driver
- **Templating**: Handlebars (HBS)
- **Session Management**: express-session
- **Deployment**: Railway.app ready

### File Structure
```
├── app.js                 # Main server application
├── package.json           # Node.js dependencies and scripts
├── railway.json          # Railway deployment configuration
├── views/
│   ├── layouts/
│   │   └── main.hbs      # Main layout template
│   ├── index.hbs         # Anonymous messaging page
│   ├── admin.hbs         # Admin dashboard
│   └── conversation.hbs  # Individual conversation view
└── replit.md             # This documentation file
```

### Database Schema
- **conversations**: Stores unique session IDs and timestamps
- **messages**: Stores all messages with conversation references and admin reply flags

### Key Features
1. **Anonymous Messaging**: Users can send messages without registration
2. **Session Tracking**: Each user gets a unique session for conversation continuity
3. **Admin Interface**: Complete dashboard at `/admin` for message management
4. **Reply System**: Admin can reply to any conversation
5. **Responsive Design**: Works on mobile and desktop devices

### URLs
- `/` - Main anonymous messaging interface
- `/admin` - Admin dashboard to view all conversations
- `/admin/conversation/:id` - View specific conversation and reply

### Environment Variables Required
- `DATABASE_URL` - PostgreSQL connection string
- `SESSION_SECRET` - Session encryption key (optional, has default)
- `PORT` - Server port (defaults to 5000)

## Deployment Instructions for Railway
1. Connect your Railway account to this repository
2. Railway will automatically detect the Node.js project
3. Set environment variable `DATABASE_URL` to your PostgreSQL connection string
4. Deploy - Railway will use the `railway.json` configuration automatically

## User Preferences
- Clean, modern UI with gradient design
- Mobile-responsive layout
- Clear separation between user and admin interfaces
- Anonymous session management without user registration