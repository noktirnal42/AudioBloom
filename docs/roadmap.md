# AudioBloomAI Roadmap

This is the public product roadmap for AudioBloomAI. Source code, internal
release engineering notes, signing details, and model-development experiments
are kept private.

## Current Release

The current public release is **AudioBloom v3.2.0**.

v3.2.0 promotes the stabilized Milkdrop shell, final source selector,
projector/Syphon workflow, Deck B crossfader, setlists, media layer controls,
and local experimental audio-semantics features into one public release.

Highlights:

- microphone/interface, all-app audio, and single-app audio capture
- explicit source-type and target pickers
- Milkdrop/projectM-first visual renderer
- Deck B A/B staging, per-deck gain, blend modes, and crossfader controls
- optional camera media layer
- favorites, ratings, history, queued-next preset, auto-advance, and saved setlists
- projector, clean output, and Syphon output workflows
- setup/help copy for Microphone, System Audio Recording, and Camera permissions
- experimental preset assistant for intent/mood-driven setlist drafts

## Near-Term Focus

- App Store launch and TestFlight feedback.
- Workflow polish for first-run setup, permission recovery, and source selection.
- More preset-library ergonomics for large Milkdrop collections.
- More validation with VJ hosts such as OBS, Resolume, TouchDesigner, and VDMX.
- Continued tuning of Deck B, projector, Syphon, and camera-layer performance.

## Experimental AI / ML Direction

AI and ML work should improve the visualizer workflow instead of distracting
from it. The public direction is:

- keep audio analysis local by default
- avoid sending microphone, system audio, camera frames, presets, or setlists to
  the developer
- use semantic audio cues only where they improve transitions, preset steering,
  and live performance control
- keep experimental controls clearly labeled until they are ready for default use

## Planning Principles

### Stabilize the flagship path first

New work should prefer:

- preset workflow quality
- output workflow quality
- transition stability
- performance and recoverability

over broad renderer experimentation.

### Keep AI behind product value

AI / ML work should only move forward when it improves:

- preset selection
- transition quality
- live performance control
- library organization
- camera-driven visuals

### Keep public and private surfaces separate

The public GitHub repository is for product information, support, privacy,
Pages, and wiki content. The source code and internal documents remain local and
private.
