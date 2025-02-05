This project is a real-time video chat application built using WebRTC for peer-to-peer communication, WebSockets for signaling, and React.js for the frontend. Users can join a lobby, enter a room, and establish a direct video connection with another user.

-Technology Stack: Uses WebRTC for peer-to-peer video communication, WebSockets (Socket.io) for signaling, and React.js for the frontend.
-LobbyScreen Functionality:
   -Users enter their name (email) and hobbies (room ID) to join a chat.
   -Emits a "room:join" WebSocket event to connect users to a room.
   -Redirects users to the RoomPage upon successful connection.
-RoomPage Responsibilities:
   -Manages WebRTC connections and peer-to-peer video streaming.
    -Handles offer-answer exchange, ICE candidate negotiation, and media transmission.
    -Uses ReactPlayer to render real-time video streams.
-Signaling Process:
    -User joins a room and sends an offer to the remote peer.
    -Remote peer responds with an answer, completing the WebRTC handshake.
-Backend WebSocket Server:
    -Solely handles signaling (offer, answer).
    -Does not process video data—WebRTC transmits media directly between peers.

    ---------------------------------------------------------------------------------

In Simple Words:
 This project is a real-time video chat application using WebRTC for peer-to-peer video calls, WebSockets for signaling, and React.js for the frontend. Users start at the LobbyScreen, where they enter their name and room ID to join a chat. When they submit, a WebSocket event (`"room:join"`) connects them to a room and redirects them to the RoomPage. The RoomPage manages video calls by setting up a WebRTC connection between users. It handles offer-answer exchange, ICE candidate negotiation, and media streaming, ensuring a smooth video call experience. The backend WebSocket server is only used for signaling, while the actual video stream is transmitted directly between users (P2P). The app uses React Router to navigate between screens. Future improvements can include better error handling, TURN server support, and UI enhancements. This setup ensures low-latency, high-performance video communication.
 ------------------------------------------------------------------------------------

 To start the project
 - cd client -> npm start
 - cd server -> npm start
