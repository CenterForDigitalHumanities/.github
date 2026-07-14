# TPEN3 — New Annotation Platform

**Repository:** [CenterForDigitalHumanities/TPEN](https://github.com/CenterForDigitalHumanities/TPEN)  
**Live URL:** [three.t-pen.org](https://three.t-pen.org) (in development)  
**Status:** In development

## What it is

TPEN3 is the next-generation platform for transcription, annotation, and image-based markup. It succeeds TPEN 2.8 and brings modern tooling — a responsive SPA frontend, a Node.js API backend, and new capabilities for scholarly annotation.

## Project structure

```
TPEN/
├── api/            # Node.js API backend (routes, controllers, database)
├── web/            # SPA frontend (HTML, CSS, JavaScript)
├── scripts/        # Build and deployment helpers
└── tests/          # Test suites
```

Key interaction patterns:

- **Frontend → API.** All data operations (load project, save annotation, create layer) go through the API, not direct database calls.
- **Canvas-first UI.** The image canvas is the primary workspace; tools orbit around it.
- **Layered annotations.** Annotations are grouped into layers (transcription, commentary, metadata) that can be toggled independently.

## Setup for development

```bash
# Clone the repository
git clone https://github.com/CenterForDigitalHumanities/TPEN.git
cd TPEN

# Install API dependencies
cd api
npm install
cd ..

# Start the API server
# (requires MongoDB — see .env.example for configuration)
npm start

# Open the frontend
# Serve web/ via any static file server
npx http-server web/ -p 3000
```

### Required services

- **MongoDB** — data store for projects, annotations, and users. Can run locally or via a connection string.
- **TPEN 2.8 archive** — read-only access to legacy projects (for import and migration). This is provided by the team.

### Configuration

Copy `api/.env.example` to `api/.env` and fill in:

- Database connection string
- TPEN 2.8 archive endpoint
- Authentication secrets

## Common contribution areas

### Frontend (`web/`)

- Canvas tools and interaction
- UI components (panels, modals, toolbars)
- Responsive layout and accessibility
- New annotation types and layer controls

### API (`api/`)

- New endpoints for tools and features
- Database query optimization
- Authentication and permission flows
- Project import/migration tools

### Cross-cutting

- **Testing** — unit tests for API routes, integration tests for frontend interactions
- **Documentation** — inline code docs, user-facing guides
- **Performance** — large canvas rendering, annotation list pagination

## Useful files to know

| File | Purpose |
|------|---------|
| `api/routes/` | API endpoint definitions |
| `web/js/` | Core JavaScript modules |
| `web/index.html` | Entry point for the SPA |
| `web/css/` | Stylesheets |

## Testing

```bash
# API tests
cd api
npm test

# Frontend (open in browser and check console)
# No formal test runner yet — manual testing via http://localhost:3000
```

## Branching and PRs

- Work on a named branch off `main`.
- Open a PR targeting `main`.
- Describe your change: what changed, why, and how to test it.
- Request a reviewer from the core team.

## Contact

- Repository owner: Center for Digital Humanities, Saint Louis University
- See the [Contributing Guide](/CONTRIBUTING.md) for general contribution conventions.
