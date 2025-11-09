# Gatherly - A Real-Time Video Conferencing Application Gatherly is a modern, full-stack video conferencing application built from the ground up to emulate the core functionality of platforms like Zoom and Google Meet. It allows users to create, join, and participate in multi-user video meetings directly from their web browser, using the power of WebRTC for low-latency, peer-to-peer communication. ![Gatherly Home Screen](https://i.imgur.com/3gXqg0z.png) --- ## Features - **Instant Meeting Creation:** Generate a unique, 6-character room ID with a single click to start a new meeting. - **Easy Joining:** Join an existing meeting using a room ID or a direct invitation link. - **Shareable Invite Links:** Easily invite others to your meeting with a simple, copy-and-paste URL. - **Pre-Join Lobby:** A lobby screen allows users to preview their camera, set their display name, and confirm their audio/video devices are working before entering the call. - **Real-Time Video & Audio:** High-quality, low-latency video and audio streaming directly between participants using WebRTC. - **Dynamic Video Gallery:** A responsive grid layout that automatically adjusts to the number of participants in the call. - **Screen Sharing:** Share your entire screen with other participants in the meeting. - **Participant Management:** View a real-time list of all attendees in a toggleable side panel. - **Interactive Controls:** - Mute / Unmute Microphone - Start / Stop Camera - Raise / Lower Hand with a visual indicator. - **Text Chat:** A simple, real-time text chat is available in a side panel for in-meeting communication. - **Secure Leaving:** A confirmation dialog prevents users from accidentally leaving the meeting. --- ## Technology Stack The application is built with a modern, separated frontend and backend architecture. #### Frontend - **React:** A JavaScript library for building dynamic, component-based user interfaces. - **TypeScript:** Adds static typing to the project for improved code quality and developer experience. - **Vite:** A high-performance development server and build tool that provides instant transpilation and hot-reloading. - **Tailwind CSS:** A utility-first CSS framework for rapidly styling the user interface. - **Socket.IO Client:** The client-side library for connecting to the backend signaling server. #### Backend (Signaling Server) - **Node.js:** A JavaScript runtime environment for executing the server-side code. - **Express.js:** A minimal web framework for Node.js, used to set up the basic server. - **Socket.IO:** A library that enables real-time, bidirectional, event-based communication for handling the WebRTC signaling logic. #### Core Protocol - **WebRTC (Web Real-Time Communication):** The browser technology that enables peer-to-peer streaming of video, audio, and data without the need for plugins. --- ## Project Structure The project is organized into two main directories: - **/backend**: Contains the Node.js signaling server. This server's only job is to manage rooms and pass connection messages between clients. It does **not** handle any video or audio streams. - **/frontend**: Contains the entire React client-side application that runs in the user's browser. --- ## Local Setup and Running Instructions To run this project on your local machine, you will need to have **Node.js** and **npm** installed. You will need to run the backend and frontend in two separate terminals. ### 1. Backend Server Setup First, let's get the signaling server running.
bash
# 1. Navigate into the backend directory
cd backend

# 2. Install the required dependencies
npm install

# 3. Start the server
npm start

# The server will start on http://localhost:3001
# Keep this terminal running!
### 2. Frontend Application Setup Now, in a **new, separate terminal**, get the user interface running.
bash
# 1. Navigate into the frontend directory
cd frontend

# 2. Install the required dependencies
npm install

# 3. Start the Vite development server
npm run dev

# The Vite server will provide you with a URL, usually http://localhost:5173
### 3. You're Ready to Go! Open your web browser and navigate to the URL provided by the Vite server (e.g., http://localhost:5173). You can now create a meeting, and even test the multi-user functionality by opening the same link in multiple browser tabs or sharing the local network link with a friend on the same Wi-Fi. --- ## Future Enhancements - **Cloud Deployment:** Deploy the backend to a service like Render and the frontend to Netlify to make the application publicly accessible. - **User Authentication:** Add a full user login/signup system to secure meetings. - **Persistent Chat:** Integrate a database to save and retrieve chat history. - **TURN Server Configuration:** Implement a TURN server to improve connection reliability for users behind restrictive firewalls.
