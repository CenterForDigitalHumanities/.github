# Export TPEN — Static Project Export Tool

**Repository:** [CenterForDigitalHumanities/ExportTPEN](https://github.com/CenterForDigitalHumanities/ExportTPEN)  
**Live URL:** [export.t-pen.org](https://export.t-pen.org)  
**Status:** Mature and actively used

## What it is

A simple web app that takes a TPEN 2.8 project and exports it as a static, standalone directory of files — HTML pages, JSON data, and images. The result can be hosted anywhere without a database.

## Project structure

```
ExportTPEN/
├── index.html          # Main app page (UI + logic)
├── export.html         # Export status page
├── js/                 # JavaScript modules
├── css/                # Stylesheets
└── images/             # Static assets
```

The entire app is a single `index.html` with inline JavaScript and CSS — simple to modify, no build step required.

## Setup for development

```bash
# Clone the repository
git clone https://github.com/CenterForDigitalHumanities/ExportTPEN.git
cd ExportTPEN

# Serve via any static file server
npx http-server . -p 8080
```

Open `http://localhost:8080`. The app calls the TPEN 2.8 API, so you need network access to `t-pen.org`.

## How it works

1. User provides a TPEN 2.8 project ID or URL.
2. The app fetches project data from the TPEN 2.8 API (pages, layers, annotations, images).
3. It generates static files:
   - `index.html` — viewable project page
   - `project.json` — complete project data
   - `page-N.json` — per-page annotation data
   - `images/` — cached page images
4. The result is downloadable as a ZIP or savable to a filesystem.

## Common contribution areas

- **Export format improvements** — better JSON structure, new file types
- **UI polish** — clearer progress indicators, error messages
- **Edge cases** — large projects, missing resources, special characters
- **Documentation** — what the exported files look like and how to use them

## Testing

1. Start the local server
2. Open the app in your browser
3. Enter a real TPEN 2.8 project URL or ID
4. Watch the export progress and inspect the output
5. Open the generated `index.html` to verify it renders

Use small projects for quick iteration. The live site at `export.t-pen.org` is always available for comparison.

## Branching and PRs

- Work on a named branch off `main`.
- Open a PR targeting `main`.
- Describe your change and what you tested.
- Request a reviewer from the core team.

## Contact

- Repository owner: Center for Digital Humanities, Saint Louis University
- See the [Contributing Guide](/CONTRIBUTING.md) for general contribution conventions.
