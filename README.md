# Lance & Spur — Jousting Derby

A 3D medieval horse-racing game with a jousting twist: race a grass turf course on
horseback and **couch your lance** to knock rivals out of the saddle as you pull
alongside them. Drain a rival's health and they spin out.

Single-file HTML5 game built with [Three.js](https://threejs.org/) (loaded from a CDN).
No build step — just open `index.html`.

## Play

- **W** — gallop · **S** — rein in / back · **A / D** — steer
- **Space** — couch lance & strike · **Shift** — spur (boost, drains stamina) · **B** — brace
- Mobile: on-screen touch controls

Two tracks (Tourney Green, Highland Run), health/spin-out combat, catch-up, WebAudio
music & SFX, and a settings menu (volume, graphics, difficulty, time-of-day).

## Deploy

Static site — Vercel serves `index.html` directly (`outputDirectory: "."`). Pushes to
`main` auto-deploy.
