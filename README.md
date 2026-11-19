# Mixit Bil Arabi

Mixit Bil Arabi is a community song-building platform and record label for the Middle East. Creators post beats, lyrics, melodies and instrument parts. AI matches them into crews, or the community remixes them into full songs. Every contributor agrees a royalty split upfront, and the best songs get signed. Invite-only in the UAE and KSA.

## What's in this repo

`index.html` is a clickable prototype of the platform. It is one self-contained file with no build step. It uses sample creators and sample music that the browser generates with the Web Audio API.

| Screen | What it shows |
|---|---|
| Invite and sign-up | Invite-code gate (demo code `MIXIT-DXB-0412`), creator profile setup, or explore as a guest |
| Discover | Beats, lyrics, melodies and instrument parts, filtered by type, dialect and mood |
| AI Match | Pick a starting piece and get a proposed crew, with the reasons for each match and the royalty split it would create |
| Upload | Post a piece, including a real audio file, and get a SHA-256 proof of creation with a timestamp |
| Songs | Every song is a tree of versions. Play any version, mute layers, and add your own layer |
| Deals | Songs move from Rising to In review to Offer sent to Signed, ranked by a signal score |
| Profile | A creator's pieces, the songs they're on, and their share of each song |

There is a language switch between English and Arabic, and the Arabic version is laid out right to left.

### How royalty splits work in the prototype

Each new layer's share is agreed before the layer is added, and earlier contributors are diluted in proportion. For example, a beat starts at 100%. When lyrics join at 30%, the beat drops to 70%. When a melody then joins at 25%, the beat has 52.5%, the lyrics 22.5% and the melody 25%. The label's share at signing is left as a placeholder because it hasn't been decided yet.

## Run it

Open `index.html` in a browser. To serve it locally instead:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

To share it as a website, turn on GitHub Pages under **Settings → Pages**, with the source set to the `main` branch and the `/ (root)` folder. GitHub Pages works on public repositories, or on private ones with a paid GitHub plan.

## Status

This is a prototype for demos and investor conversations. Nothing is stored on a server: the demo data lives in the viewer's browser and can be reset from the Profile page. The production plan is in the project's research notes (`creator-platform-tech-stack.md`).
