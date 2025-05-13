A simple real-time chat application demonstrating how to build chat systems using both Native WebSocket and Socket.IO, with a React.js frontend.

 Native WebSocket (ws package)
 Socket.IO (socket.io)
 React.js Frontend (shared UI for both)

Project Structure
pgsql
Copy
Edit
real-time-chat-app/
├── native-websocket/     # Native WebSocket server
│   └── server.js
├── socket-io/            # Socket.IO server
│   └── server.js
├── client/               # React frontend app
│   └── react-app/
│       ├── public/
│       └── src/
├── README.md             # This file
└── .gitignore

 Getting Started
Prerequisites:
Node.js (v14 or higher)

npm (Node Package Manager)

Installation Steps
1️. Install React App Dependencies
bash
Copy
Edit
cd client/react-app
npm install
2️. Install Native WebSocket Server Dependencies
bash
Copy
Edit
cd ../../../native-websocket
npm install ws express
3️. Install Socket.IO Server Dependencies
bash
Copy
Edit
cd ../socket-io
npm install express socket.io


 Build React Frontend
Before running any server, build the React frontend so both backends can serve it.

bash
Copy
Edit
cd ../client/react-app
npm run build
This will create a production build in /build folder.

Run Native WebSocket Server
bash
Copy
Edit
cd ../../../native-websocket
node server.js
Open in browser: http://localhost:3001

Run Socket.IO Server
In a separate terminal window/tab:

bash
Copy
Edit
cd socket-io
node server.js
Open in browser: http://localhost:3002

How it Works
React frontend connects to either:

Native WebSocket (ws://localhost:3001)

Socket.IO (http://localhost:3002)

Auto-detects based on port:

3001 → Native WebSocket

3002 → Socket.IO

Real-time chat messages are sent and received instantly.

Features
Real-time bi-directional communication
React.js frontend with clean UI
Simple styling (CSS)
Supports both Native WebSocket & Socket.IO seamlessly

Notes
Make sure you don't run both servers on the same port.

Native WebSocket is lighter but lower-level.
Socket.IO adds extra features (rooms, reconnections, etc.).


