# ♟️ Multiplayer Chess Game

A Python-based real-time multiplayer chess game that allows two players to connect and play over a network. It features a clean graphical user interface built with **Pygame** and uses **socket programming** to handle communication between clients and the server. The game strictly follows standard chess rules and includes a matchmaking lobby system.

---

## 📌 Description

Multiplayer Chess Game is an educational and practical project designed to demonstrate the integration of **network programming**, **game logic**, and **GUI development** in Python. Players connect to a central server and are matched in pairs to begin a game of chess. The game state is synchronized between the two clients using a custom messaging protocol, and all valid moves, checks, and checkmates are enforced according to chess rules.

---

## 🧱 Project Structure

This project is organized into three main modules:

- **`server/`** — Handles socket connections, game sessions, and lobby management.
- **`client/`** — Runs the user interface, handles player input, and sends/receives messages from the server.
- **`common/`** — Shared logic between server and client, including rules, constants, and communication format.

---

## 📁 Folder Structure

```
📦 root/
├── client/
│   ├── images/           # Chess piece images and UI assets
│   ├── client.py         # Handles socket connection and incoming messages
│   ├── gui.py            # Pygame GUI rendering and player input
│   └── utils.py          # Utility functions for the client
│
├── common/
│   ├── chess_logic.py    # All game logic: valid moves, checks, checkmate
│   ├── constants.py      # Global constants (e.g., host/port, board size)
│   └── message.py        # Message structure used by client and server
│
├── server/
│   ├── server.py         # Main server loop; manages connections
│   ├── game_session.py   # Game logic for an active match
│   ├── lobby.py          # Manages player queue and pairing
│   └── utils.py          # Server-specific helper functions
```

---

## 🔧 Requirements

- Python 3.8+
- [Pygame](https://www.pygame.org/)
- [python-chess](https://pypi.org/project/python-chess/)

Install dependencies using pip:

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run

### 1. Start the Server

In one terminal window, run:

```bash
python -m server.server
```

This will start the socket server that listens for incoming client connections and manages matchmaking.

### 2. Start the Client

In another terminal window (or on another machine), run:

```bash
python -m client.gui
```

Repeat this step to start a second client so two players can be paired and start playing.

> ✅ Ensure that both clients can reach the server's IP and port defined in `common/constants.py`.

---

## 📄 Documentation

A full guide to the design, logic, message formats, and architecture can be found here:  
📎 [View Full Documentation](https://docs.google.com/document/d/1lUAXp2R_7SiedBwF9k8MTPPfWv9EDPAtt2fK_3woCqc/edit?usp=sharing)

---

## 🎮 Features

- ♟ Standard chess rules enforced via `python-chess`
- 🌐 Multiplayer mode with real-time synchronization
- 🕹️ Interactive UI using Pygame (drag & drop pieces, highlight moves)
- 🔄 Turn-based system with move validation
- 🧠 Modular logic for easy extension (add bots, timers, undo, etc.)
- 📡 Lobby system for automatic matchmaking

---

## 🚧 Future Enhancements

- Add player timers and turn limits
- Implement AI mode for single player
- Add a spectate mode for observers
- Chat system between players
- Persistent leaderboard and player stats

---

## 🤝 Contributing

Pull requests and issue reports are welcome! Please make sure to follow clean coding practices and write descriptive commit messages.

---

## 🧪 Run Tests (Optional)

Coming soon: unit tests for chess logic and networking using `pytest`.

---

## 📜 License

This project is open-source and available under the MIT License.

---
