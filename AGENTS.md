# AGENTS

## Overview
Diagram-Editor-Pro-2 is a self-contained diagram editor implemented in a single HTML file: `diagram-editor-pro-multilink.html`. It renders a canvas-based editor with node templates, linking, undo/redo, grid snapping, and light/dark themes.

## Code Structure
- **State**: `state` keeps nodes, selection, theme, grid, zoom, and render flags.
- **Utilities**: `utils` provides helpers for ID generation, snapping, cloning, and coordinate conversion.
- **Node Management**: `nodeManager` creates, deletes, duplicates, and validates nodes.
- **Rendering**: `render()` draws grid, shapes, and links on the `<canvas>` and is scheduled via `requestAnimationFrame`.
- **Interaction**: `interaction` tracks dragging, selection, panning, and linking modes.
- **History**: `historyManager` implements undo and redo via JSON snapshots.

## Conventions
- Use **two spaces** for indentation; avoid tabs.
- Use `const`/`let` and terminate statements with semicolons.
- Prefer arrow functions and object spread syntax.
- Keep CSS and JS inline within the HTML file and update CSS variables for theming.
- When adding features, update related sections: state, utilities, managers, and render.
- Maintain accessible markup (`aria-*` labels, keyboard shortcuts, focus management).
- Follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages.

## Development
- No build step or external dependencies. Open `diagram-editor-pro-multilink.html` in a modern browser to run.
- Run `npm test` (currently prints "missing script: test") before committing to acknowledge the lack of automated tests.
