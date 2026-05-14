# Getting Started

## Requirements

- macOS 13.0 or later
- Microphone permission for mic/interface capture
- System Audio Recording permission for app/system audio capture
- Camera permission only if you want the live camera layer

## Install

1. Join the [AudioBloomAI TestFlight](https://testflight.apple.com/join/AyHQBwgR), if testing slots are still available.
2. Install AudioBloomAI from TestFlight.
3. Launch AudioBloomAI.

The App Store button currently links to Apple's App Store landing page and will
be replaced with the product page after approval.

## First Setup

On first launch, AudioBloom opens a setup guide that walks through the practical path to a working visualizer:

- choose `Microphone / Interface`, `All App Audio`, or `Single App Audio`
- choose the matching microphone, system output, or running app from the second picker
- grant the matching macOS permission
- start or restart capture
- stay on the recommended Milkdrop / projectM renderer for presets, setlists, projector, Syphon, and camera texture workflows

You can reopen the same guide from `Settings > Setup`.

## Settings Layout

Settings are organized around workflows:

- `Setup` gets first-run users to a live input and recommended renderer.
- `Input` contains source routing, permission status, source gain, noise gate, and capture diagnostics.
- `Visuals` contains workspace appearance and Milkdrop/projectM playback controls.
- `Presets` contains auto-advance, setlists, library state, and preset-file actions.
- `Output` contains Syphon, Clean output, and Projector status.
- `Experimental` contains camera/AI lab features, including optional camera vision masks, local audio semantics, and future ML-assisted controls.

If you choose `All App Audio` or `Single App Audio`, grant **System Audio Recording** access in System Settings and relaunch the app if macOS asks you to.

## First Visualizer Run

1. Complete `Settings > Setup`.
2. Keep the renderer on `Milkdrop / projectM` for the richest workflow.
3. Open the preset browser or import a Milkdrop pack.
4. Use the Control Pane for live changes once capture is running.
