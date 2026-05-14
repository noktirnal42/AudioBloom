# Integrations

## Projector Output

AudioBloom can send the visualizer to a second display while keeping controls on the main screen. This is useful for TVs, projectors, and performance setups.

Common setup:

- keep the main AudioBloom window on your laptop screen
- use the top toolbar or Control Pane to open a clean output window for capture/AirPlay
- use `Control Pane > Output > Projector` when a separate display is connected
- keep presets, reactivity, media texture, and audio controls on the main screen
- stop projection from the Control Pane when you are done

The projector surface is render-only. It does not include the control pane, preset browser, or other workspace chrome. By default, Clean and Projector outputs mirror the composed main workspace frame so projected output and Syphon feeds match what you see in the app, including transitions, dual-preset blends, and media texture layers. Disable `Mirror main workspace into Clean and Projector outputs` in Settings only when you intentionally want those windows to render independently.

## Syphon

Syphon publishing is bundled with AudioBloom and is available from the Milkdrop renderer without a separate user install.

Syphon can publish one render surface at a time:

- **Main workspace** publishes the primary render surface in the main AudioBloom window.
- **Clean output window** publishes the separate render-only window. Open the clean output window before choosing this source. With mirroring enabled, it receives the same composed frame as the main workspace.
- **Projector** publishes the dedicated projector surface. Start projection before choosing this source. With mirroring enabled, it receives the same composed frame as the main workspace.

Runtime status:

- **Live** means the selected surface is active and publishing Milkdrop frames.
- **Waiting** means Syphon is enabled but the selected surface is not active yet, such as Clean output closed or Projector stopped.
- **Missing** means AudioBloom could not find its bundled `Syphon.framework` or a system-installed fallback.
- **Disabled** means Syphon publishing is off.

Performance notes:

- AudioBloom has no hard launch dependency on Syphon. If the framework is missing, the renderer continues normally and skips publishing.
- Starting a projector automatically selects Projector as the Syphon source; closing it returns the source to Main workspace.
- Mirroring is enabled by default for Clean and Projector outputs. Independent output rendering can drift from the main workspace because each OpenGL view owns a separate projectM instance.
- Start at **60 FPS** for normal Syphon workflows. If you run Deck B compositing, camera media layers, scene-aware transitions, and Syphon together on a laptop, expect roughly one busy CPU core and lower Syphon to **30 FPS** if the host VJ app or projector path shows stutter.
- Keep **Mirror Main to outputs** enabled for performance sets unless you intentionally need independent output rendering. Mirroring is the safest path for keeping Main, Clean, Projector, and Syphon visually matched.
- Choose **Main workspace** as the Syphon source for the lowest-friction setup. Choose **Clean** or **Projector** only when that surface is already open/live and you specifically want the external feed to follow that output role.

## Media Texture Layer

AudioBloom can capture a live camera feed and use it as the first supported media texture layer in the Milkdrop renderer. The layer model is source-based so still images and movie clips can be added later without replacing the renderer overlay path.

When `Camera vision analysis` is enabled, AudioBloom samples a small luma grid from the camera feed on the camera capture queue. That produces optional motion, edge-density, and silhouette signals for the media texture shader without placing analysis work inside the frame-critical render path.

Controls live in:

- `Settings > Experimental`

You can toggle:

- capture foundation
- active camera device
- selected media source
- media texture layer
- layer strength
- blend mode
- vision mask analysis

## Experimental AI / ML Lab

The `Experimental` tab also includes early AI/ML-oriented toggles:

- semantic preset steering for local buildup, drop, breakdown, and section-change events
- scene-aware transitions that consume semantic transition urgency without adding work to the render loop
- camera vision analysis for media-layer motion, edge, and silhouette masks
- LLM mood prompting

Audio semantics are produced by an on-device, CoreML-ready classifier boundary. The current build uses lightweight local heuristics over the existing reactivity stream until a trained bundled CoreML model is available, keeping realtime preset and transition decisions local by default.

## Preset Assistant Boundary

The Presets tab includes a prototype assistant for high-level preset organization. Type a mood or performance intent, generate a draft, inspect the suggested presets with tags and reasons, then save the draft as a normal editable setlist.

This workflow is intentionally separate from realtime rendering. The current build uses local preset metadata as an inspectable fallback; a future LLM provider should only replace the draft-suggestion step and should never be required for frame rendering, audio capture, Syphon, or projector output.

These are experimental controls and should be treated as a lab surface rather than finalized product behavior.
