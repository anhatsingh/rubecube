# rubecube

A full‑stack demo project to create, display, scramble, and solve a Rubik's Cube in the browser. The goal is to showcase frontend and backend skills: an interactive 3D cube UI, move generation & animations, a solver service, and APIs to run/record solutions.

## Features
- Interactive 3D Rubik's Cube UI (rotate faces, scramble, input moves).
- Automatic solver that returns a move sequence for a given cube state.
- REST/WebSocket API to submit states and stream solver progress.
- Demo pages for visualization, step-by-step playback, and solution export.
- Focus on clean frontend architecture and a well-documented backend.

## Tech stack
- Frontend: React + Three.js for 3D rendering.
- Backend: Node (Express) to expose solver endpoints.
- Solver: implement standard cube representation and known algorithms (e.g., Kociemba) or a BFS/IDA* solver for demonstration.

## Repo layout
- frontend/ — UI app (React, build & dev scripts)
- backend/ — API & solver implementation
- docs/ — architecture, API docs, design notes
- scripts/ — dev & deployment helpers

## Quick start
Prerequisites: Node.js

Frontend
```sh
cd frontend
npm install
npm run dev
```

Backend (example with Python)
TBD

## Development notes
- Keep cube state and move notation standardized across frontend and backend.
- Add unit tests for cube operations and solver correctness.

## Contributing
- Open issues for bugs/feature requests.
- Follow consistent commit messages and add tests for new logic.
- Document major design decisions in docs/.