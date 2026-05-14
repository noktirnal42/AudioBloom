# Renderers and Presets

## Renderer

AudioBloom uses a single renderer: Milkdrop / `projectM`. It supports:

- importable preset libraries
- ratings and favorites
- recent history
- queued-next presets
- traversal modes
- safer app-side transitions on macOS
- selectable transition styles
- projector and Syphon integration
- optional media texture layer with live camera and vision-derived masks
- preset assistant drafts for intent/mood based setlist building

## Milkdrop Preset Workflow

The preset browser supports:

- search by preset name and pack
- favorites
- ratings
- recent filter
- back / forward history
- queued-next preset
- import and open preset folder
- Deck B A/B compositor workflow

Auto-advance traversal controls live in the Control Pane with the other live
performance controls. The preset browser is intentionally focused on search,
filtering, library status, and direct preset selection.

Preset libraries live in:

```text
~/Library/Application Support/AudioBloom/Presets/
```

## Transitions

Native `projectM` second-preset worker transitions are disabled on macOS in the current runtime because they were unstable. AudioBloom now uses a safer custom transition layer on top of hard cuts.

Transition v2 supports four app-managed styles:

- `Dissolve`: clean crossfade for calmer sessions
- `Cinematic`: subtle zoom, vignette, and motion smear
- `Psychedelic`: chromatic split, noise breakup, and focus glow
- `Beat Punch`: a faster, more rhythmic variant that uses beat confidence when available

When beat-aware timing is enabled, strong detected beats shorten the overlay duration so manual and auto-advance switches feel more musical without re-enabling the native projectM transition worker.

When `Scene-aware transitions` is enabled, AudioBloom also blends in local semantic audio urgency from buildup, drop, breakdown, and section-change detection. That signal is produced outside the renderer frame path and only changes transition timing and styling inputs.

## Preset Assistant

The Presets settings tab includes a high-level assistant workflow for library organization:

- enter an intent or mood, such as `dark bassy build into a bright drop`
- generate a preview of matching presets
- inspect suggested tags, reasons, packs, and scores before accepting anything
- save the draft as a normal editable setlist

The assistant is not part of the realtime renderer. The current implementation uses local preset and pack metadata so it works without network or model availability. Future LLM integration should remain bounded to offline setlist/tag drafting and leave render timing to local audio semantics and CoreML.

## Deck B A/B Compositor

AudioBloom includes a Deck B workflow for Milkdrop presets. Deck B is rendered through a separate `projectM` instance and composited by AudioBloom, which avoids the unstable native `projectM` second-preset worker on macOS.

It supports:

- assigning a staged secondary preset
- enabling or disabling the Deck B compositor independently from staging
- independent Deck B previous/random/next navigation
- independent Deck A and Deck B pre-crossfader gain
- a true A/B crossfader
- queueing
- swapping
- blend amount control
- browser and Control Pane visibility for the staged deck
