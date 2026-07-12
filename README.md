# Lance & Spur — Jousting Derby

**▶ Play: https://lance-and-spur.vercel.app**

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

## Evermoor Glade (prototype)

An early vertical slice of a **cozy fantasy life-sim** (think Animal Crossing with
magic) lives at [`/glade`](https://lance-and-spur.vercel.app/glade). Wander an
enchanted glade, chat with the villagers (Pip the Mushroomfolk, Bramble the
Fox-Mage, Dewdrop the Frog), gather flowers/mushrooms/crystals/lanterns, and
decorate your corner of the world. Full day–night cycle with night-blooming lights.

- **WASD** walk · **drag** to look · **E** talk · **F** gather · **1–4** select item · **Q** place
- Same single-file Three.js setup as the main game — see `glade.html`.

> **Mud & Ember**, the pottery studio game that used to live at `/pottery`, has
> moved to its own project — [`draphael123/mud-and-ember`](https://github.com/draphael123/mud-and-ember).

## Deploy

Static site — Vercel serves `index.html` directly (`outputDirectory: "."`). Pushes to
`main` auto-deploy.
