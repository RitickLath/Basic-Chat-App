# WebSocket Chat Application

This is a simple WebSocket-based chat application that allows multiple users to join a specific chat room and exchange messages in real time. The project consists of a backend server built with Node.js and the `ws` library, and a frontend built using React.

---

## Features

- Real-time communication using WebSocket.
- Room-based chat functionality (users can join a specific room).
- Dynamic message broadcasting to all users in the same room.

---

## Getting Started

### Prerequisites

Ensure you have the following installed:

- **Node.js** (v14 or higher)
- **npm** (Node Package Manager)
- **React** (installed via `create-react-app` or a similar tool)

---

## Installation

### Backend Setup

1. Navigate to the backend directory (if applicable):
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install ws
   ```
3. Start the WebSocket server:
   ```bash
   node server.js
   ```
   The WebSocket server will start on `ws://localhost:8080`.

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the React application:
   ```bash
   npm start
   ```
   The React application will start on `http://localhost:3000`.

---

## File Structure

### Backend (`server.js`)

- **WebSocketServer:** Listens for connections on port 8080.
- **`User` Interface:** Represents a user with their WebSocket connection and room ID.
- **`allSockets` Array:** Tracks all connected users and their room assignments.
- **Message Handling:**
  - `join`: Adds a user to a specific room.
  - `chat`: Broadcasts a message to all users in the same room.

### Frontend (`App.js`)

- **WebSocket Client:** Connects to the WebSocket server.
- **Room Joining:** Sends a `join` message to associate the user with a specific room.
- **Message Sending:** Sends chat messages to the server, which are then broadcast to the room.
- **Message Display:** Shows received messages in a user-friendly interface.

---

## Usage

1. Start both the backend server and the frontend React app.
2. Open the React app in a browser (default: `http://localhost:3000`).
3. Enter a message in the input box and click **Send message** to broadcast it to all users in the same room.
4. Open multiple browser tabs or devices to simulate multiple users.

---

## Example Scenarios

1. **Joining a Room:**

   - A user joins the room `red` by default when the app is loaded.

2. **Real-Time Messaging:**
   - Messages sent by one user are broadcast to all users in the same room.

---

## Dependencies

- **Backend:**
  - `ws`: WebSocket library for server-side communication.
- **Frontend:**
  - React: JavaScript library for building the user interface.

---

## Future Improvements

1. Add support for multiple rooms with a dynamic room creation feature.
2. Implement user authentication for secure communication.
3. Improve error handling for better debugging and user feedback.
4. Add typing indicators and message timestamps.
5. Store chat history in a database for persistence.

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---

## Acknowledgments

- The `ws` library for simplifying WebSocket integration.
- React for creating a seamless frontend experience.

---
