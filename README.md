# Start Page

A standalone browser start page built as a single `index.html` file.

It includes a large clock, configurable search engine selector, customizable shortcut tiles, local persistence, and touch-friendly drag-and-drop reordering.

## Features

- Single-file app with no build step
- Large live clock and date display
- Search with selectable engines
- Custom shortcut grid with up to 12 entries
- Add, edit, delete, and reset shortcuts
- Drag-and-drop reordering on desktop and touch devices
- Local persistence with `localStorage`
- Embedded SVG favicon

## Usage

Open `index.html` directly in a browser, or serve it from a local/static web server.

For the best cross-browser behavior, especially around favicons and local security restrictions, serving over HTTP is recommended.

Examples:

```powershell
# Python
python -m http.server 8080

# Node.js
npx serve .
```

Then open:

```text
http://localhost:8080
```

## Customization

The page stores its state in `localStorage`, including:

- saved shortcuts
- selected search engine
- favicon fallback cache

Using **Reset defaults** restores the default shortcuts and clears all saved `localStorage` data for the page.

## Browser Notes

- The page includes handling for browser differences around overscroll and touch dragging.
- If opened via `file://`, some browsers may restrict remote favicon requests or log security warnings. This is expected browser behavior rather than an app error.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

Copyright (c) 2026
