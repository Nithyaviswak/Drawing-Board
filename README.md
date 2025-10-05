Drawing Board - A Real-Time Collaborative Whiteboard
📖 Introduction
This project is a real-time, collaborative drawing application built from the ground up using WebSockets. It provides a shared canvas where multiple users can draw, add shapes, and see each other's changes live. The application is designed with a clean, intuitive interface and is built with a lightweight stack, making it both powerful and easy to understand.

✨ Features
Real-Time Collaboration: All actions are instantly synchronized across all connected clients using a WebSocket backend.

Versatile Drawing Tools:

Pen: For freehand drawing.

Eraser: To remove freehand strokes.

Move Tool: Select and reposition shapes on the canvas.

A Wide Array of Shapes: Instantly add common shapes to the canvas:

Square, Rectangle, Circle, Triangle

Parabola, Cone, Cylinder

Full Customization:

Full-Spectrum Color Picker: Choose any color for your pen and shapes.

Adjustable Brush Size: Control the thickness of your strokes.

Clear Canvas: A simple one-click button to clear the entire board for everyone.

Responsive Design: The layout adapts to different screen sizes for a seamless experience.

🛠️ Tech Stack
This project uses a simple and effective combination of modern web technologies:

Frontend:

HTML5: For the basic structure and <canvas> element.

Tailwind CSS: For a utility-first approach to styling and a clean UI.

JavaScript (ES6+): To handle all client-side logic, drawing, and communication.

Backend:

Node.js: As the JavaScript runtime environment.

ws Library: A popular, lightweight library for handling the WebSocket server.

🚀 Getting Started
To get a local copy up and running, follow these simple steps.

Prerequisites
Make sure you have Node.js and npm installed on your machine. You can check by running:

node -v
npm -v

Installation & Setup
Clone the repository or download the files into a new directory.

Set up the Backend Server:

Open your terminal and navigate to the project directory.

Initialize a package.json file:

npm init -y

Install the required WebSocket library:

npm install ws

Start the server:

node server.js

You should see the confirmation message: WebSocket server started on port 8080. Keep this terminal window running.

Launch the Frontend:

In your file explorer, find and double-click the index.html file.

This will open the Drawing Board in your default web browser.

Open the index.html file in multiple browser tabs or windows to simulate multiple users and test the real-time collaboration!

⚙️ How It Works
The application's real-time functionality is based on a simple client-server architecture:

Client Action: When a user performs an action (e.g., draws a line, adds a shape), the frontend JavaScript captures the event data (coordinates, color, tool type, etc.).

Send to Server: This data is packaged into a JSON object and sent to the Node.js backend via the active WebSocket connection.

Broadcast: The WebSocket server receives the message and immediately broadcasts it to every other connected client, without saving any data itself.

Receive and Render: All other clients receive the JSON message, parse it, and use the data to execute the drawing or shape manipulation function on their own canvas, ensuring all boards are synchronized.
