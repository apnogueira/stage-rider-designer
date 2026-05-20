# Stage Designer V2

Interactive stage plotting and patching tool for live audio planning.

## Overview

Stage Designer V2 is a single-file web app that helps you:

- Place instruments and snakes on a virtual stage
- Connect sources to snake inputs and outputs
- Manage drum mic sub-inputs (including mono/stereo overheads)
- Route and adjust cable paths visually
- Export layout data and production-friendly reports

## Features

- Single interaction mode: click to select, drag to move, pin-to-pin connect
- Drag-and-drop cable creation plus click-to-connect
- Snake I/O with realistic grouping and pin labeling
  - Inputs shown as numbers
  - Outputs shown as letters (A, B, C, ...)
  - Reports include output letter and numeric index
- Zoom and pan workspace controls
- Cable hover/selection highlighting
- Rider save/load support
- Report preview and PDF print flow

## Project Structure

- `stage-designer-v2.html`: main app (HTML, CSS, JavaScript in one file)

## Getting Started

1. Clone or download this repository.
2. Open `stage-designer-v2.html` in a modern browser.
3. Start placing items from the palette and connect using the blue pins.

No build step or dependency installation is required.

## Usage Notes

- Drag instrument body to move it.
- Click any instrument to edit properties.
- Start a connection from a pin, then click or drag to another valid pin.
- Shift + mouse wheel pans horizontally.

## Exporting

- **Save Rider**: saves project rider JSON (`<project>.rider.json`)
- **View Report**: opens printable report in a new tab
- **Export PDF**: opens print dialog for PDF export using project-based report name

## Browser Compatibility

Designed for current Chromium-based browsers and modern Firefox/Safari versions.

## License

Add your preferred license here (for example, MIT).
# Stage-Ryder-Designer
