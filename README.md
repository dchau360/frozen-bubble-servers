# Frozen Bubble — Public Server List

Community-maintained list of public servers for [Frozen Bubble SDL2](https://github.com/dchau360/frozen-bubble-sdl2). The game fetches this list automatically on startup so players can find servers without entering an IP manually.

---

## Adding Your Server

1. Fork this repo
2. Edit `serverlist-1` and add your server (see format below)
3. Open a pull request

### Format

One entry per line. Comments start with `#`.

```
# host:port  Display name (optional)
game.example.com:1511  My Server (desktop/Android)
game.example.com:443   My Server (browser)
```

- **Port 1511** — native TCP for desktop (Linux, macOS, Windows) and Android clients
- **Port 443** — secure WebSocket (`wss://`) for browser (itch.io / WASM) clients

If your server supports both, add two lines — one for each port. Players on native clients will use 1511; browser players will use 443.

### Requirements

- The server must be publicly reachable
- Browser (`wss://`) entries require a valid TLS certificate on a real domain — see [SetupServer.md](SetupServer.md) for the full setup guide
- Native (TCP) entries work with a plain IP address or domain, no SSL needed

---

## Setting Up a Server

See [SetupServer.md](SetupServer.md) for step-by-step instructions covering:

- Docker Compose setup (fb-server + nginx)
- Getting a free SSL certificate with Let's Encrypt
- Connecting native and browser clients
- Certificate renewal

---

## Current Servers

See [`serverlist-1`](serverlist-1).
