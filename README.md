# CCTV Frontend Application

## Overview
This repository contains the frontend application for a CCTV monitoring system.  
It provides a user interface for viewing live camera feeds, managing camera settings, and playing back recorded footage stored in the cloud.  
The frontend communicates with the backend via REST APIs and WebSockets for real-time updates.

---

## Key Features
- User authentication and authorization
- Live video streaming (HLS)
- Camera management interface (add, edit, remove cameras)
- Playback of recorded video footage
- Real-time updates using WebSockets
- Responsive UI for desktop and tablet

---

## Tech Stack
- **Frontend Framework:** React.js
- **UI Components:** Tailwind CSS / MUI (optional)
- **Video Playback:** Video.js or native HTML5 `<video>` tag
- **State Management:** React Context / Redux (optional)
- **API Communication:** Axios / Fetch
- **Real-time Communication:** Socket.IO client
- **Build & Deployment:** Vite or Create React App
- **Cloud Integration:** AWS S3 + CloudFront (for recorded footage)

---

## Project Structure
```
src/
 ├── components/      # Reusable UI components (buttons, modals, cards)
 ├── pages/           # Page views (Dashboard, Camera Management, Playback)
 ├── services/        # API calls and data fetching
 ├── context/         # React context for global state management
 ├── utils/           # Helper functions
 ├── App.js           # Root application component
 ├── index.js         # Entry point
```

---

## Environment Variables
Create a `.env` file in the root directory:

```env
REACT_APP_API_URL=http://localhost:3000/api
REACT_APP_WS_URL=http://localhost:3000
REACT_APP_AUTH_TOKEN_NAME=auth_token
```

**Do not commit `.env` files to the repository.**

---

## Getting Started

### Prerequisites
- Node.js (v18 or later)
- npm or yarn
- Backend server running (cctv-backend)

### Install Dependencies
```bash
npm install
```

### Run Development Server
```bash
npm start
```

Server will start at:
```
http://localhost:3001
```

### Build for Production
```bash
npm run build
```
The `build/` folder can be deployed to any static hosting service or cloud provider.

---

## Security Notes
- Do not expose backend API keys in frontend code
- Use HTTPS for production API calls
- JWT tokens should be stored securely (localStorage/sessionStorage)
- Validate user inputs to avoid XSS

---

## License
This project is licensed under the **MIT License**.

---

## Notes
This frontend is under active development.  
Feature scope and UI design may evolve as the system matures.
