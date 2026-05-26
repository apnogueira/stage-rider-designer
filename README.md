# Stage Ryder Designer

Stage Ryder Designer is a browser-based stage plotting, audio patching, and reporting tool for live production planning.

It is designed to be practical for real-world stage and monitor workflows: quick visual layout, fast pin-to-pin routing, mix console and snake mapping, and production-ready reports.

## What This Project Is

This project is a single-page web app that runs directly in the browser from one main file:

- index.html contains UI, styles, and application logic
- images folder contains instrument, mixer, stagebox, stand, and accessory artwork

No build toolchain is required.

## Core Goals

- Build stage layouts quickly with drag-and-drop
- Map signal flow from source to destination with clear pin semantics
- Support both musical and technical planning workflows
- Preserve and reload rider files reliably
- Export visuals and printable reports for production handoff

## Feature Highlights

### 1) Stage Layout and Visual Planning

- Instrument placement by drag-and-drop from categorized palettes
- Visual stage with audience direction and scalable dimensions
- Zoom and pan controls for dense or large setups
- Light and dark theme support
- Stage color customization
- Optional stage grid visibility
- Auto-updating stage dimensions and scale readout

### 2) Stage Builder Mode

- Toggle between live patch mode and stage builder mode
- Add room and platform shapes (rectangle and circle)
- Resize and recolor stage shapes from properties panel
- Label each shape for venue-specific planning
- Optional steps flag for rectangular shapes

### 3) Layer Ordering Controls

- Header Layers menu with:
  - Bring Forward
  - Bring to Front
  - Send Backward
  - Send to Back
- Immediate visual reorder on click
- Works on selected instrument in live mode
- Works on selected shape in stage builder mode

### 4) Rich Instrument and Device Library

Palettes include:

- Instruments (drums, strings, keys, vocals, brass)
- Snakes
- Mixers
- Stageboxes
- PA and monitoring
- Accessories
- Stands

Representative built-in device coverage includes:

- XR18
- X32 family (full, compact, rack)
- M32 and M32R
- WING family (full, compact, rack)
- S32 and S16 stageboxes
- Monitor devices like P16 and PM1

### 5) Connection and Cable System

- Pin-based routing between valid endpoints
- Click-to-connect workflow from source pin to destination pin
- Cable type aware routing (XLR, Jack TS, Jack TRS, Speakon, Ethernet, MIDI, Digital)
- Automatic cable typing constraints by pin role and device
- Connection hover and focus highlighting
- Orthogonal cable paths with route handles
- Multi-cable bus grouping for parallel routes
- Visual route editing by dragging cable handles

### 6) Snake and Patch Infrastructure

- Snake devices with stage mode and cable mode views
- Input and output labeling designed for live patch workflows
- Legacy and modern pin mapping normalization on load
- Stage return handling for snakes with output banks

### 7) Mixer, Stagebox, and I/O Modeling

- Configurable mixer input breakdown:
  - XLR-only input banks
  - Combo input banks
  - Aux jack input banks
- Output modeling by family:
  - XLR outputs
  - Main outputs when relevant
  - Aux jack outputs
  - Ultranet and AES50 system outputs
- Stagebox behavior aligned to console expansion workflows

### 8) Instrument Properties and Behavior

- Editable label, channel/input text, and notes
- Connector side controls
- Size slider and reset-to-default
- Angle control with rotary knob
- Stereo signal mode where supported
- Input/output mode toggles for custom I/O devices
- Speaker connector mode controls for through chains

### 9) Mic Pickup Assignment System

- Per-pin mic model assignment UI
- Works across vocal, instrument, and drum contexts
- Built-in mic model library
- User-managed custom mic models (add and remove)
- Automatic connector compatibility guardrails for mic-assigned paths
- Drum mic mapping with dedicated drum pin model

### 10) Mic Stand Planning

- Mic stand options for supported instrument types
- Stand count control and clamping by instrument capability
- Drum-specific stand assignment tied to selected drum mic inputs
- Mic stand badge overlay on stage items for quick visual reference
- Stand category in palette for physical stand planning on stage map

### 11) Drumkit Workflow Enhancements

- Drum input checkbox matrix (kick, snare, toms, overheads, etc.)
- Stereo overhead handling with separate left/right pin outcomes
- Automatic pruning of invalid drum-related connections when drum setup changes
- Drum mic stand assignment matrix linked to selected drum inputs

### 12) Save, Load, and Data Persistence

- Save rider to JSON
- Save As support with file naming controls
- Load rider from file picker
- Compatibility path for older rider data through normalization and defaults
- Project name persisted in layout data
- Dirty state tracking to warn before destructive actions
- Panel preference persistence and custom mic option persistence in local storage

### 13) Reporting and Export

- Report generation from current layout and routing state
- Report options dialog for output customization
- Structured signal-path reporting including endpoint labels
- Cable hop and route visibility in report output
- Feature-specific summaries (including stand and DI related totals)
- Export PNG
- Export PDF flow

### 14) Keyboard and Interaction Quality

- Keyboard shortcuts for common editing actions
- Selection-aware deletion behavior
- Undo support with snapshot history
- Touch and mouse support paths for drag, pan, and control adjustments
- Mobile menu support for constrained viewports

## Typical Workflow

1. Set project name and stage appearance
2. Drag musicians, consoles, snakes, and outputs to the stage
3. Configure per-device properties (labels, channels, connector sides, stereo, notes)
4. Add pin-to-pin routing and adjust cable paths
5. Assign mic models and stand planning details
6. Use Layers controls to resolve visual overlap
7. Save rider JSON for later revisions
8. Export PNG/PDF and generate report for production handoff

## Project Structure

- index.html: Entire application UI, CSS, and JavaScript logic
- images/: Device and icon assets used by palettes and stage rendering
- README.md: Project documentation
- CODEOWNERS: Ownership metadata

## Run Locally

No dependency install is required.

Use one of these methods:

1. Open index.html directly in a modern browser
2. Or run a lightweight static server and open the served page

## Browser Notes

- Best experience on modern Chromium-based browsers
- Modern Firefox and Safari are also supported for standard usage
- Some save/load picker capabilities depend on browser File System Access APIs and gracefully fall back where unavailable

## Data and Compatibility Notes

- Rider layout save format currently writes version 4
- Loader normalizes many missing fields for backward compatibility
- Array order is part of visual layer order and is persisted in saves

## Limitations and Future Ideas

Potential future improvements:

- Multi-select transform and bulk editing
- Snap-to-grid and alignment tools
- Enhanced collaboration and diff view between rider revisions
- Optional plug-in model for additional console families

## License

Add your preferred license for distribution and contribution policy.
