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

## Mud & Ember (prototype)

A **free-build pottery studio** with the full production pipeline lives at
[`/pottery`](https://lance-and-spur.vercel.app/pottery). Mobile-first (one-thumb
portrait play, mouse works too): wedge the air out of the clay, centre it on the
wheel, throw a pot with drag gestures — thin walls wobble and collapse, and the
clay dries while you fuss — trim at leather-hard, survive the bisque fire, dip it
in glaze, then gamble everything on the glaze fire. Survivors go on the studio
shelf.

- Pick what to make (cup/bowl/vase/jug/amphora or freeform) — a guide silhouette
  appears on the wheel and your sketch match is scored
- **Tap** to wedge · **hold** to centre · **drag sideways** to shape · **drag up** at the rim to pull taller
- **Sponge** re-wets (soft clay slumps) · **trim** evens walls · both kiln passes roll real risk from your shortcuts
- A brick kiln in the corner with a full firing cinematic (door, peephole glow, spark reveal)
- Three clay bodies (stoneware and porcelain unlock as you fire pieces), glaze finishes
  (gloss/satin/speckled) with pooling and drips, photo mode with PNG export
- The shelf is **persistent** — fired survivors are still there next visit
- Settings menu (volume, graphics, clay forgiveness, camera sway), skippable intro
- Same single-file Three.js setup — see `pottery.html`.

## Deploy

Static site — Vercel serves `index.html` directly (`outputDirectory: "."`). Pushes to
`main` auto-deploy.
