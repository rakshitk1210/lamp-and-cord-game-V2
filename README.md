# Lamp & Cord

A pixel-art mini-game where you plug a lamp into a wall outlet by timing a cord throw across a room full of obstacles. Built with React + Vite, deployed on Netlify.

**[Play it live →](https://lamp-cord-game-uist.netlify.app)**

---

## Gameplay

A lamp sits on a table. An outlet is on the far wall. Your cord swings up and down — press **Space** (or say **"Go"** in voice mode) to throw it toward the outlet. Land it in the target zone to light the lamp and advance to the next level.

You get **3 tries per level**. Miss all three and you restart the level.

### Controls

| Mode | Action |
|------|--------|
| **Keyboard** | `Space` — throw the cord |
| **Voice / Sound** | Say *"Go"* or make any loud sound |

Switch between modes anytime via the **⚙ Settings** button.

---

## Levels

| # | Name | Challenge |
|---|------|-----------|
| 1 | Level 1 | Open room — learn the timing |
| 2 | Level 2 | Coat rack blocks part of the path |
| 3 | Level 3 | Shelf, a bouncing cat, and growing fireplace flames |
| 4 | Level 4 | Cuckoo clock pendulum swings into the path |
| 5 | Level 5 | Two plants that grow and shrink continuously |
| 6 | Level 6 | A spinning fan cuts across the cord trajectory |

Difficulty increases each level: the aim oscillates faster, the hit tolerance shrinks, and obstacles move more aggressively.

### Quick Level Jump

Press **1–6** on the keyboard to jump directly to any level.

---

## Tech Stack

- **React 19** — UI and game state
- **HTML5 Canvas** — pixel-art rendering (all graphics drawn programmatically, no image assets)
- **Web Audio API** — microphone input for voice/sound control mode
- **Vite 7** — dev server and build tool
- **Netlify** — hosting with SPA redirect rules

---

## Running Locally

```bash
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173).

```bash
npm run build    # production build → dist/
npm run preview  # preview the production build
```

---

## Project Structure

```
src/
  LampGame.jsx    # main game: canvas rendering, physics, input, all 6 levels
  SpritesPage.jsx # dev page to preview individual sprites (/sprites route)
  App.jsx         # route: / → LampGame, /sprites → SpritesPage
```

---

## Research Context

This game was built as a stimulus for a **UIST user study** exploring novel input modalities (keyboard vs. voice/sound) in casual game interactions. The `Lamp & Cord_ User Testing Guide.pdf` in the repo root contains the study protocol and task instructions.
