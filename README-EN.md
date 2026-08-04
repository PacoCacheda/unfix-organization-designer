# unFIX Organization Designer

> Visual organization designer based on Jurgen Appelo's **unFIX** model.
> A single HTML file. No build, no server, no dependencies.

**▶️ [Open the tool](https://pacocacheda.github.io/unfix-organization-designer/)**

*[Versión en español](README.md)*

---

## What it is

A canvas tool for mapping how an organization is — or could be — structured, using the [unFIX](https://unfix.com) pattern library: Bases, Crews, Forums, Turfs, Leagues, Crowds and everything in between.

Drag patterns from the side library, nest them inside containers, connect them, and annotate each element with its mission, people and maturity state. The tool checks the result against the model's structural rules and flags what looks off.

## Features

- **Full unFIX pattern library** — 10 families and 38 subtypes, each with a description and a link to the official docs:
  - **Crew Types** (7): Value Stream, Experience, Facilitation, Capability, Platform, Governance, Partnership
  - **Base Types** (4): Fully Integrated, Strongly Aligned, Loosely Aligned, Fully Segregated
  - **Forum Types** (10): Business Model, Channel, Customer Journey, Functional, Market, Organizational, Product, Regional, Seasonal, Technological
  - **Turf Types** (4): Team of Teams, House, Product Area, Business Unit
  - **Scaling · League**: League, Clusters (7 types), Assembly
  - **Scaling · Crowd**: Crowd, Coalition, Congress
- **Real containment** — drop a Crew inside a Base or a Turf and it belongs to it; moving the container moves everything inside.
- **Three connection types** — Value flow (solid), Dependency (dashed) and Alignment (dotted, double arrow).
- **Maturity states** — Turmoil, Forming, Performing and Reforming, encoded by color and borders.
- **Design diagnostics** — checks the canvas against unFIX structural rules and summarizes element and headcount totals.
- **Per-element inspector** — name, type, mission, lead, number of people, notes and connections.
- **Export** — re-importable JSON, 2× PNG and vector SVG, editable in Figma, Illustrator or Inkscape.
- **Bilingual** — full UI in Spanish and English.
- **Auto-save** in the browser (`localStorage`); nothing leaves your machine.
- **Interactive guided tour** on first run.

## Usage

Nothing to install. You have two options:

1. **Online** — open [pacocacheda.github.io/unfix-organization-designer](https://pacocacheda.github.io/unfix-organization-designer/).
2. **Local** — download `index.html` and double-click it in any modern browser. It works offline (only the fonts load from Google Fonts; without them it falls back to system fonts).

### Keyboard shortcuts

| Action | Shortcut |
|---|---|
| Zoom | `Mouse wheel` |
| Pan the canvas | `Drag the background` |
| Disable grid snapping | `Alt` while dragging |
| Connection types | `1` `2` `3` |
| Back to select | `V` |
| Cancel connection | `Esc` |
| Delete | `Del` |
| Undo / Redo | `Ctrl+Z` / `Ctrl+Shift+Z` |
| Duplicate | `Ctrl+D` |

## About the unFIX model

unFIX is **not a framework**: it's a pattern library. Nothing is mandatory, the approach is bottom-up, and the model is fractal — the same patterns repeat at Base, League and Crowd level.

The model is the work of **Jurgen Appelo** and is documented at **[unfix.com](https://unfix.com)**. This project is an independent, unofficial tool with no affiliation to unFIX or its author. If the model interests you, the official site is the source.

## Technology

HTML, CSS and JavaScript in a single ~2,700-line file. SVG rendering. Zero dependencies, zero build, zero backend.

## License

[MIT](LICENSE) for the tool's code. The unFIX model and its terminology belong to their respective authors.
