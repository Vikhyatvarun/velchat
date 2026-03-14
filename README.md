# Velchat — Secured P2P Chat

> Zero-server. Zero-logs. Zero trust required.

**Velchat** is a fully encrypted, peer-to-peer chat application that runs entirely in the browser — no server, no accounts, no message storage. Two people connect directly using WebRTC, exchange messages through an end-to-end encrypted data channel, and leave no trace when they're done.

---

## How It Works

Velchat uses **WebRTC DataChannels** for direct browser-to-browser communication. The connection is bootstrapped through a manual signaling handshake — you copy-paste a short connection code between peers (or scan a QR code). Once connected, all messages travel directly between browsers and never touch a server.

---

## Features

- 🔒 **End-to-end encrypted** — WebRTC DTLS encryption by default, no plaintext ever leaves your device
- 🚫 **No server, no accounts** — pure P2P; nothing is stored or logged anywhere
- 📎 **File transfers** — send files up to 16MB directly to your peer
- 🔍 **Message search** — search through your local chat history
- 💾 **Export chat** — save a copy of the conversation locally
- ⚠️ **Panic button** — instantly wipes the entire session and chat history
- 🎨 **Themeable** — six color themes (green, blue, purple, red, yellow, gray)
- 📱 **Mobile-friendly** — responsive layout with touch optimizations and proper keyboard handling
- 🔔 **Typing indicators** — real-time typing status sent over the data channel
- ✓ **Read receipts** — see when your messages have been seen
- 📊 **Connection stats** — live latency, uptime, and data transferred

---

## Usage

1. Open `index.html` in any modern browser — no build step, no dependencies
2. **Host** clicks "I'M HOST", copies the generated offer code
3. **Peer** clicks "I'M JOINING", pastes the code, and copies back their response code
4. **Host** pastes the response code and completes the connection
5. Chat securely — the connection is direct and encrypted

Works entirely offline after the initial code exchange (e.g. via a side channel like Signal or email).

---

## Tech Stack

| Layer | Technology |
|---|---|
| Transport | WebRTC DataChannel (DTLS encrypted) |
| Signaling | Manual copy-paste / QR code (no signaling server) |
| NAT Traversal | Google STUN servers |
| UI | Vanilla HTML, CSS, JavaScript — single file, zero dependencies |

---

## Privacy Model

- No accounts, no login
- No server receives your messages
- No analytics, no telemetry
- Chat history exists only in browser memory — gone on refresh
- The panic button clears everything immediately

---

## Browser Support

Any modern browser with WebRTC support: Chrome, Firefox, Safari, Edge. Works on desktop and mobile.

---

## License

MIT
