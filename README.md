# WebRTC Demo - Video Chat Room

A simple, single-page WebRTC video chat application that allows multiple people to connect in virtual rooms for audio, video, and text chat.

## Features

- 🎥 **Video Chat**: Real-time video streaming using WebRTC
- 🎤 **Audio Chat**: Crystal clear audio communication
- 💬 **Text Chat**: Send text messages to all participants
- 🚪 **Room-based**: Join specific rooms via URL query string
- 🎨 **Modern UI**: Clean interface styled with Tailwind CSS
- 📱 **Responsive**: Works on desktop and mobile devices

## Usage

### Quick Start

1. Open `index.html` in a web browser
2. Enter a room name or use a URL with a room query parameter:
   ```
   index.html?room=my-room-name
   ```
3. Allow camera and microphone access when prompted
4. Share the URL with others to have them join your room

### Room Access

- **Create/Join a room**: Navigate to `index.html?room=yourRoomName`
- **Share with friends**: Send them the same URL to join your room
- **Multiple rooms**: Use different room names for different conversations

### Controls

- **Video On/Off**: Toggle your video stream
- **Audio On/Off**: Mute/unmute your microphone
- **Text Chat**: Type messages in the chat box and press Enter or click Send

## Technical Details

### Technologies Used

- **PeerJS**: Simplifies WebRTC peer-to-peer connections
- **Vanilla JavaScript**: No frameworks required
- **Tailwind CSS**: Utility-first CSS framework for styling
- **WebRTC APIs**: Native browser support for real-time communication

### How It Works

1. Each user gets a unique peer ID when joining a room
2. PeerJS handles the WebRTC signaling via their free server
3. Users discover each other through localStorage-based peer discovery
4. Direct peer-to-peer connections are established for media and data
5. Video/audio streams and chat messages flow directly between peers

### Browser Compatibility

Requires a modern browser with WebRTC support:
- Chrome/Edge 56+
- Firefox 44+
- Safari 11+
- Opera 43+

## Development

This is a standalone HTML file with no build process required. Simply:

1. Clone the repository
2. Open `index.html` in a web browser
3. Start testing!

### Hosting

You can host this application on any static web server:
- GitHub Pages
- Netlify
- Vercel
- Any web server serving static files

## Security Notes

- The application uses PeerJS's free signaling server
- For production use, consider hosting your own PeerJS server
- All video/audio/data streams are encrypted via WebRTC
- Peer discovery uses localStorage (same-origin only)

## License

MIT License - feel free to use and modify as needed.