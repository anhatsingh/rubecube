# rubecube

A full‑stack demo project to create, display, scramble, and solve a Rubik's Cube in the browser. The goal is to showcase frontend, backend, and AI skills: an interactive 3D cube UI, move generation & animations, a solver service, and APIs to run/record solutions.

## Core focus
This project gives equal weight to:
- Web development (interactive 3D UI, state management, APIs, deployment)
- AI & algorithms (solver research, ML/heuristics/GA experiments, model inference)

## Features
- Interactive 3D Rubik's Cube UI (rotate faces, scramble, input moves).
- Automatic solver that returns a move sequence for a given cube state.
- REST/WebSocket API to submit states and stream solver progress.
- Demo pages for visualization, step‑by‑step playback, and solution export.
- Experiments with ML, Genetic Algorithms, and classical algorithms for solving.
- Focus on clean frontend architecture and a well-documented backend/AI pipeline.

## Tech stack
- Frontend: React + react-three-fiber (Three.js under the hood) for 3D rendering.
- Backend: Node (Express) to expose solver and orchestration endpoints.
- AI: Python (models, training, inference), experiments with Kociemba, IDA*, Genetic Algorithms, or learned heuristics.

## Repo layout
- frontend/ — React app (react-three-fiber), build & dev scripts
- backend/ — Node API & orchestration code
- ai/ — models, training code, inference services, experiment notebooks
- docs/ — architecture, API docs, design notes, requirements
- scripts/ — dev & deployment helpers
- tests/ — unit & integration tests

## Quick start
Prerequisites: Node.js, Python 3.8+

Frontend
```sh
cd frontend
npm install
npm run dev
```

Backend (Node)
```sh
cd backend
npm install
npm run dev
```

AI (Python)
```sh
cd ai
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
# run training/inference scripts or start an inference server
python -m ai.server  # example
```

## APIs & integration notes
- Standardize cube state representation and move notation across frontend, backend, and AI.
- Recommended endpoints:
  - POST /solve — return solution moves
  - WS /solve/stream — stream solver progress
  - POST /ai/infer — run a model-based suggestion or heuristic
- Ensure move parity and notation compatibility between modules.

## Development notes
- Frontend: aim for time-to-first-render <1s p95.
- Backend: target response time <200ms p90 for core endpoints.
- CI/CD, Dockerized environments, and cloud hosting are expected.
- Add unit tests for cube operations, solver correctness, and AI components.

## Contributing
- Open issues for bugs/feature requests.
- Add tests for new logic and experiments.
- Document model experiments, datasets, and hyperparameters in docs/ and ai/README.md.

## License
Add a LICENSE file (e.g., MIT) as appropriate.