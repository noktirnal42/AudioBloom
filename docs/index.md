---
layout: default
title: AudioBloom
---

<section class="hero">
  <div class="hero-copy">
    <h1>AudioBloom</h1>
    <p class="lede">
      A macOS visualizer for DJs, VJs, projection artists, and live music spaces.
      Capture the room, the system mix, or one running app, then drive Milkdrop
      visuals to projectors, Syphon hosts, and clean show outputs.
    </p>
    <div class="hero-actions">
      <a class="button primary" href="https://testflight.apple.com/join/AyHQBwgR">Join TestFlight</a>
      <a class="button secondary" href="https://www.apple.com/app-store/">Get on App Store</a>
      <a class="button secondary" href="./getting-started">Set up audio</a>
    </div>
  </div>
  <figure class="hero-media">
    <video controls playsinline preload="metadata" poster="{{ '/assets/img/audiobloom-live-hero.jpg' | relative_url }}" aria-label="AudioBloomAI promo video showing reactive audio visuals and VJ performance features">
      <source src="{{ '/assets/video/audiobloomai-promo-720p.mp4' | relative_url }}" type="video/mp4">
    </video>
    <figcaption>AudioBloomAI promo video with real app visuals and performance workflow highlights.</figcaption>
  </figure>
</section>

<section class="audience-strip" aria-label="Built for live visual performance">
  <span>DJ booths</span>
  <span>VJ rigs</span>
  <span>Gallery projections</span>
  <span>Stream visuals</span>
</section>

<section class="grid two">
  <article class="panel">
    <h2>Performance-first rendering</h2>
    <p>AudioBloom centers the Milkdrop / <code>projectM</code> path: import presets, rate favorites, queue the next visual, auto-advance, and crossfade Deck B blends without relying on unstable native projectM transition workers.</p>
  </article>
  <article class="panel">
    <h2>Audio that fits the room</h2>
    <p>Use a microphone or interface, capture the full system mix, or target one running app through Core Audio process taps. The selector shows source type first, then the matching microphone, output device, or app.</p>
  </article>
</section>

<section class="showcase">
  <figure>
    <img src="{{ '/assets/img/audiobloom-live-output.jpg' | relative_url }}" alt="A second AudioBloom live visual frame with layered geometric Milkdrop imagery">
    <figcaption>Real AudioBloom v3.2.0 output captured from the macOS app.</figcaption>
  </figure>
  <div class="showcase-copy">
    <h2>Made for visual sets, not desktop wallpaper.</h2>
    <p>AudioBloom keeps the performance path practical: load Milkdrop presets, stage a second deck, crossfade into the next look, and send the result to the room through a clean output, projector, or Syphon host.</p>
    <ul>
      <li>Source routing for microphone/interface, system mix, or one app.</li>
      <li>Deck B staging with pre-crossfader gain and blend modes.</li>
      <li>Preset browser, favorites, history, setlists, and auto-advance.</li>
    </ul>
  </div>
</section>

<section class="grid three">
  <article class="panel">
    <h2>Projector + Syphon</h2>
    <p>Mirror the composed workspace frame to Clean output, Projector, and Syphon so host apps and external displays stay aligned during transitions, Deck B blends, and camera layers.</p>
    <a href="./integrations">Output guide</a>
  </article>
  <article class="panel">
    <h2>Preset workflow</h2>
    <p>Search by preset or pack, favorite and rate visuals, revisit recent history, save setlists, and use the assistant for inspectable mood-based drafts.</p>
    <a href="./renderers-and-presets">Renderer guide</a>
  </article>
  <article class="panel">
    <h2>Local AI lab</h2>
    <p>AudioBloomAI includes experimental local audio-semantics controls for scene-aware transitions and preset steering. They are optional, on-device, and still labeled as lab features.</p>
    <a href="./roadmap">Roadmap</a>
  </article>
</section>

<section class="release-card">
  <div>
    <p class="eyebrow">Current Release</p>
    <h2>AudioBloom v3.2.0</h2>
    <p>Promotes the stabilized Milkdrop shell, final source selector, projector/Syphon workflow, Deck B crossfader, media-layer controls, and local experimental audio-semantics features into one public release.</p>
  </div>
  <ul>
    <li><a href="https://testflight.apple.com/join/AyHQBwgR">Join the free TestFlight</a></li>
    <li><a href="https://www.apple.com/app-store/">Get on App Store</a></li>
    <li><a href="./getting-started">Setup guide</a></li>
  </ul>
</section>

<section class="start-links">
  <h2>Start Here</h2>
  <a href="./getting-started">Install and route audio</a>
  <a href="https://testflight.apple.com/join/AyHQBwgR">Join TestFlight</a>
  <a href="./renderers-and-presets">Build a preset workflow</a>
  <a href="./integrations">Send visuals to a projector or Syphon</a>
  <a href="./support">Get support</a>
  <a href="./privacy">Read the privacy policy</a>
  <a href="./third-party-notices">Third-party notices</a>
  <a href="https://github.com/noktirnal42/AudioBloom/wiki">Read the wiki</a>
</section>

## Permission Model

AudioBloom needs **Microphone** permission for microphone/interface input, **System Audio Recording** permission for app/system audio capture, and **Camera** permission only when the optional live camera layer is enabled.
