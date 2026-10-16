# Startup Funding & Build System — Implementation Plan

## Scope
Build a self-contained React dashboard inside the existing Startup-Funding-2025 repository. The dashboard turns the three resource bundles into an English operating system for founders: guided phases, actionable tasks, a detailed learning/work table, search and filters, and direct GitHub links to the relevant source files.

## Implementation
- Replace the incomplete `App` import target with `src/App.tsx`.
- Add a Vite/TypeScript runtime manifest and package scripts so the project runs locally.
- Keep the UI dependency-light: React, ReactDOM, TypeScript, Vite, and plain CSS.
- Store the founder workflow, task statuses, and references as typed data in `App.tsx`.
- Persist task completion in `localStorage` so the system remains useful between sessions.
- Link reference materials to the committed GitHub paths; no source PDFs are duplicated.

## Project structure
- `src/App.tsx`: dashboard shell, workflow data, filters, phase navigation, task controls, and reference links.
- `src/index.css`: responsive visual system and component styling.
- `src/main.tsx`: React entry point.
- `public/manus-routes.json`: route declaration for the single-page dashboard.
- `package.json`, `tsconfig.json`, `vite.config.ts`: local development and build configuration.
- `README.md`: existing project overview remains the source project description.

## Design
- **Design movement:** Editorial command center — a calm, high-signal founder workspace inspired by premium research dashboards.
- **Core principles:** evidence before hype; one next action at a time; references stay visible; financial readiness is measurable.
- **Color philosophy:** warm paper background with ink navy for trust, electric blue for action, and restrained green/amber/red for status.
- **Layout paradigm:** left rail for orientation, wide working canvas for the table, and a compact right-side action summary on desktop.
- **Signature elements:** phase rail, numbered progress markers, and reference chips that expose the exact learning source.
- **Interaction philosophy:** every phase turns a concept into a deliverable; completion is explicit and persistent.
- **Animation:** subtle hover lift and progress transitions only; no distracting motion.
- **Typography:** system sans-serif with strong numeric hierarchy and compact uppercase labels.
- **Brand essence:** a practical founder operating system that connects learning resources to investor-ready evidence; disciplined, useful, direct.
