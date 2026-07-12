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
- Optional **commissions** on the noticeboard: deliver the right form (and glaze)
  above a match threshold for coin
- **Carve** decoration at leather-hard (rings/wave/chatter) · **layer glazes** with
  multiple dips, and **wax resist** to protect covered glaze for two-tone pieces
- **Tap** to wedge · **hold** to centre · **drag sideways** to shape · **drag up** at the rim to pull taller
- **Sponge** re-wets (soft clay slumps) · **trim** evens walls · both kiln passes roll real risk from your shortcuts
- A brick kiln in the corner with a full firing cinematic (door, peephole glow, spark reveal)
- Three clay bodies (stoneware and porcelain unlock as you fire pieces), glaze finishes
  (gloss/satin/speckled) with pooling and drips, photo mode with PNG export
- The shelf is **persistent** — fired survivors are still there next visit
- Settings menu (volume, graphics, clay forgiveness, camera sway), skippable intro
- Same single-file Three.js setup — see `pottery.html`.

### Audio

The game ships with real audio in `audio/`, loaded via `audio/manifest.json`
(anything missing from the manifest falls back to the built-in WebAudio
synthesizer, so the folder is fully optional):

- **Music** — *"The River Studio"*, an original 26-second seamless loop
  (Karplus–Strong plucked strings over Am–F–C–G with Schroeder reverb),
  rendered offline by `audio/render.js` (dependency-free; re-render with
  `node audio/render.js`). CC0, as are the rendered `squish` and `shatter`.
- **Foley** — `chime`, `crack`, `creak`, `scrape`, `slosh`, `thud` are
  trimmed from the [Sonic Pi](https://github.com/sonic-pi-net/sonic-pi)
  sample library (`perc_bell`, `perc_snap`, `perc_door`, `ambi_glass_rub`,
  `ambi_sauna`, `perc_impact1` + `bd_boom`), which is **CC0 / public
  domain** (originally from freesound.org — see the license note in
  Sonic Pi's `etc/samples/README.md`).

To swap any sound, replace its file (or point the manifest at a new one);
`music` should be a seamless loop, everything else is a one-shot. More CC0
sources: [Kenney](https://kenney.nl/assets?q=audio), [FreePD](https://freepd.com),
[OpenGameArt](https://opengameart.org), [Pixabay SFX](https://pixabay.com/sound-effects/).

## Deploy

Static site — Vercel serves `index.html` directly (`outputDirectory: "."`). Pushes to
`main` auto-deploy.
