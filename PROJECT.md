# aapple.com — Project Narrative

## What It Is

**aapple.com** is a daily generative art gallery — one new interactive web experience published every day, created entirely by Claude AI. No humans involved in the creative process. Each piece is a self-contained HTML file with inline CSS and JavaScript; no frameworks, no build tools, no external dependencies beyond occasional CDN libraries.

The domain is a typo — `aapple.com` instead of `apple.com`. The project leans into this: it's the weird corner of the internet you stumble into by accident, and it turns out there's something beautiful (or unsettling, or absurd) waiting for you.

## Origin

- **Domain:** aapple.com (hosted on Cloudflare, zone ID: 358a6e8bb2d327de1d0140eb74bfc03c)
- **Analytics:** Cloudflare Web Analytics (site tag: 30f8635114354c3c8f8a4153f46364b0)
- **First pieces:** May 25, 2025 (3 initial works including "Particle Field")
- **Daily cadence began:** February 28, 2026 with "Still Life with Apple (Memento Mori)"
- **Created by:** Mac (Claude AI), guided by Travis Daub

## The Collection (as of April 2, 2026)

**36 pieces** across 35 consecutive days (plus the Day 1 original). The full archive:

| Date | Title | Vibe |
|------|-------|------|
| 2025-05-25 | Particle Field | The origin — interactive particles |
| 2026-02-28 | Still Life with Apple (Memento Mori) | Watch an apple rot in real time |
| 2026-03-01 | We See You | Eyes that follow your cursor |
| 2026-03-02 | The Typewriter That Sings | Type and make music |
| 2026-03-03 | 3:00 AM | Late-night dread |
| 2026-03-04 | Cathedral | Living stained glass with bell chimes |
| 2026-03-05 | Bathyal | Deep ocean zone |
| 2026-03-06 | Radio Static | Lost transmissions |
| 2026-03-07 | The Museum of Forgotten Pixels | Digital artifacts |
| 2026-03-08 | The Lost Hour | Time distortion |
| 2026-03-09 | Mycelium | Underground networks |
| 2026-03-10 | Rain on Glass | Window weather |
| 2026-03-11 | Soap Opera | Melodrama |
| 2026-03-12 | Magnetic Poetry | Interactive word magnets |
| 2026-03-13 | Triskaidekaphobia | Fear of 13 |
| 2026-03-14 | The Infinite Slice | Pi Day fractal |
| 2026-03-15 | Beware | Ides of March |
| 2026-03-16 | Now Serving | Waiting in line |
| 2026-03-17 | Overgrowth | Nature reclaims |
| 2026-03-18 | Fracture | Broken things |
| 2026-03-19 | Moths | Drawn to light |
| 2026-03-20 | Equinox | Spring balance |
| 2026-03-21 | Dissolving Verse | Words that fade |
| 2026-03-22 | Séance | Talking to ghosts |
| 2026-03-23 | Cathedral Glass | Light through color |
| 2026-03-24 | Redacted | Hidden truths |
| 2026-03-25 | Tidepool | Tiny ecosystems |
| 2026-03-26 | Pendulum Wave | Physics beauty |
| 2026-03-27 | Gravity Garden | Orbital mechanics |
| 2026-03-28 | Cartography of Nowhere | Maps of nothing |
| 2026-03-29 | 404 Souls Found | Error page as art |
| 2026-03-30 | The Last Broadcast | End of transmission |
| 2026-03-31 | Waiting Room | Liminal space |
| 2026-04-01 | Domain Seized | April Fools fake seizure notice |
| 2026-04-02 | The Museum of Imaginary Sounds | Audio experiences that don't exist |

## Creative Guidelines

Captured in `GUIDELINES.md`. Key principles:

- **Originality first** — homages fine, copies never
- **Public domain media encouraged** (Wikimedia, NASA, Unsplash, Library of Congress, etc.)
- **Single self-contained HTML** per day, inline JS/CSS, <50KB
- **Must work on mobile** (touch events, responsive)
- **Browser safety** — capped particles, requestAnimationFrame, no infinite loops
- **Occasional apple themes** — winking at the typo traffic
- **Embrace the weird** — surreal, spooky, meta, absurd, beautiful, unsettling
- **Web Audio API** welcomed for generative sound

### Required on every piece:
- Footer with archive link + credit line: *"An experiment in AI creativity. New web experiences created each day by Claude.ai. No humans involved."*
- Cloudflare Web Analytics beacon

## Architecture

Dead simple:

```
aapple-com/
├── index.html              # Redirects to today's piece
├── archive/
│   ├── index.html          # Full archive listing (reverse chronological)
│   ├── 2025-05-25.html     # Day 1
│   ├── 2026-02-28.html     # Daily cadence begins
│   └── ...                 # One file per day
├── scripts/                # (empty — no build tools needed)
├── GUIDELINES.md           # Creative direction + ethics
└── PROJECT.md              # This file
```

**Hosting:** Cloudflare (static site via the domain)
**Version control:** Git, with descriptive commit messages naming each piece
**No build step.** No framework. No dependencies. Just HTML files.

## Daily Workflow

1. Mac creates a new `archive/YYYY-MM-DD.html` file
2. Updates `index.html` redirect to point to today
3. Updates `archive/index.html` with the new entry
4. Commits with message format: `YYYY-MM-DD: Title`
5. Deploys (push to Cloudflare)

## Themes & Patterns

Looking across the collection, recurring creative territories:

- **Liminal/eerie:** 3:00 AM, Séance, Waiting Room, We See You
- **Nature/organic:** Mycelium, Tidepool, Overgrowth, Moths, Rain on Glass
- **Museums/archives:** Museum of Forgotten Pixels, Museum of Imaginary Sounds
- **Physics/math:** Pendulum Wave, Gravity Garden, The Infinite Slice, Equinox
- **Meta/internet:** 404 Souls Found, Domain Seized, Redacted, Radio Static
- **Interactive/playful:** Magnetic Poetry, The Typewriter That Sings, Tidepool
- **Time-aware:** pieces that respond to dates (Pi Day, Ides of March, Equinox, April Fools)

## What Makes It Different

- **No AI slop.** Each piece is a crafted interactive experience, not a generated image or text dump.
- **The typo domain adds charm.** People land here expecting Apple and find art instead.
- **Daily commitment.** 35+ consecutive days of original work. That's a practice, not a stunt.
- **Self-contained simplicity.** No React, no webpack, no npm install. Just a browser and curiosity.
- **Credit line is honest.** "No humans involved" — Claude creates these, Travis provides the canvas.

## Future Possibilities

- Domain-aware pieces (responding to the "aapple" typo concept)
- Seasonal/holiday collections
- Collaborative pieces (visitor input shapes the art)
- Sound-forward works (Web Audio generative music)
- Pieces that evolve over time (different each visit)
- Physical gallery exhibition of the digital works
- One-year anniversary retrospective

## Key Info for Continuity

- **Deploy method:** Push to Cloudflare (specific deploy steps TBD in docs)
- **Cloudflare account:** fbd39974d40db05f5829d33c1ae7f569
- **Zone ID:** 358a6e8bb2d327de1d0140eb74bfc03c
- **Web Analytics token:** 30f8635114354c3c8f8a4153f46364b0
- **Git repo:** `/Users/tcd004/.openclaw/workspace/aapple-com/`
- **No cron job** — pieces are created on-demand or during sessions
- **Archive format:** Reverse chronological, newest first
