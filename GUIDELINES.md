# aapple.com — Daily Art Guidelines

## Creative Direction
- Occasionally (randomly) use an apple theme — wink at the typo traffic
- Embrace weird, surreal, even spooky pieces
- Use Web Audio API freely — generative sound, interactive audio, ambient drones
- Get meta — self-referential, breaking the fourth wall, commentary on the internet itself
- Range from beautiful to unsettling to playful to absurd

## Technical Constraints
- **Browser safety first** — cap particle counts, use requestAnimationFrame, no infinite loops
- Single self-contained HTML file per day (inline JS/CSS, no external deps except CDN libs)
- Must work on mobile (touch events, responsive canvas)
- Keep file size reasonable (<50KB per piece)
- Test-worthy: no WebGL features that crash older devices

## Structure
- Each day: `archive/YYYY-MM-DD.html`
- `index.html` redirects to today's piece
- `archive/index.html` lists all past days
- Footer on every piece: archive link + credit line

## Footer (required on every piece)
```html
<div class="footer">
  <a href="/archive/">archive</a>
  <div class="credit">An experiment in AI creativity. New web experiences created each day by Claude.ai. No humans involved.</div>
</div>
```

## Analytics (required on every piece)
Add this just before `</body>` on every page:
```html
<!-- Cloudflare Web Analytics --><script defer src='https://static.cloudflareinsights.com/beacon.min.js' data-cf-beacon='{"token": "30f8635114354c3c8f8a4153f46364b0"}'></script><!-- End Cloudflare Web Analytics -->
```

## Idea Bank
- Particle systems, physics sims, gravity wells
- Recursive geometry, fractals, L-systems
- ASCII/text art animations
- Fake OS interfaces, glitch art, corrupted UIs
- Interactive sound toys, generative music
- Optical illusions, impossible objects
- Cellular automata, Conway variations
- Type-to-create experiences
- Webcam mirror effects (with permission prompt)
- "This page is watching you" paranoia pieces
- Countdown to nothing, loading bars that never finish
- Apples — falling, rotting, orbiting, pixelated, photorealistic
- Pages that respond to time of day or device orientation
- Fake error pages that are actually art
- Pieces that evolve the longer you stay
