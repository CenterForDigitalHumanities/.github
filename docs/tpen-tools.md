# tpen.tools — Utilities and Services

**Repository:** [CenterForDigitalHumanities/tpen.tools](https://github.com/CenterForDigitalHumanities/tpen.tools)  
**Live URL:** [tpen.tools](https://tpen.tools)  
**Status:** Mature and actively used

## What it is

A collection of web-based tools for interacting with TPEN data — project management, annotation editing, image processing, and interoperability utilities. Each tool is a standalone page that can be embedded or opened directly.

## Project structure

```
tpen.tools/
├── index.html          # Landing page / tool directory
├── tools/              # Individual tool pages
│   ├── project/        # Project management tools
│   ├── annotation/     # Annotation editing tools
│   ├── image/          # Image processing utilities
│   └── export/         # Data export helpers
├── js/                 # Shared JavaScript modules
├── css/                # Stylesheets
└── images/             # Static assets
```

## Setup for development

This is a static site — no build step or backend required.

```bash
# Clone the repository
git clone https://github.com/CenterForDigitalHumanities/tpen.tools.git
cd tpen.tools

# Serve via any static file server
npx http-server . -p 8080
```

Open `http://localhost:8080` in your browser. Most tools call the TPEN 2.8 API directly, so they work as-is — though some endpoints may require authentication.

## Common contribution areas

- **New tools** — add a page under `tools/` that solves a specific task
- **Shared modules** — factor out common patterns into `js/` for reuse
- **Tool improvements** — better UX, edge-case handling, accessibility
- **Documentation** — each tool should describe its inputs, outputs, and limitations

## Testing

Tools are tested by opening them and exercising the core workflow:

1. Start the local server (`npx http-server`)
2. Open the tool page
3. Perform the primary action (load a project, save an annotation, export data)
4. Check the browser console for errors

Some tools depend on the TPEN 2.8 API — make sure you can reach `t-pen.org` from your environment.

## Branching and PRs

- Work on a named branch off `main`.
- Open a PR targeting `main`.
- Describe your change and link the tool URL.
- Request a reviewer from the core team.

## Contact

- Repository owner: Center for Digital Humanities, Saint Louis University
- See the [Contributing Guide](/CONTRIBUTING.md) for general contribution conventions.
