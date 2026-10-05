# Wall Street Quest

A CFA Level I learning game in a single HTML file. You climb from Intern to Charterholder across ten city districts, one per CFA Level I topic. Each district teaches through a guided story, a simulation where the concept decides the outcome, and an exam-style test.

## Run it

Play online at https://thienhuonqq.github.io/cfa_game/ or open `index.html` in a browser. No build step and no install. The 3D city loads three.js from cdnjs; without WebGL the game falls back to a flat district directory.

## What's built (v0.2)

- **3D city (new in v0.2):** walk your analyst around a plaza ringed by the 10 districts. WASD/arrow keys or an on-screen joystick, drag to turn the camera, click or tap a building to walk there and go in. Knowledge orbs give pop quizzes; the Margin Clerk (Review Boss), Exam Hall, Binder Kiosk, BA II Plus Terminal, Weak Spot Board and Records Office stand in the plaza.
- **Levels 1–10:** Intern → Charterholder. Each level changes your character's outfit, from hoodie and lanyard to the Charterholder's glow. The Exam Hall opens at Level 3.

- **Engine:** city map of all 10 districts with official topic weights, XP and ranks, streaks, confidence-calibrated scoring, a weak-spot tracker with 1/3/7-session spaced repetition, a Review Boss, formula cards, a BA II Plus TVM trainer, and a timed exam mode.
- **District 7, Bond Bridge (Fixed Income):** five-chapter Learn lab (duration balance beam, price–yield curve with convexity gap), a Pricing Booth and Rate Shock Desk to play, and a 10-question CFA-style test.
- **Districts 1–6 and 8–10:** locked placeholders, wired to the engine.

## Saving progress

Progress is kept in memory only. Use **Save / load** to copy a `WSQ1.` progress code and paste it back next time.

## Extending the question bank

Questions live in the `QUESTIONS` array in `index.html`:

```js
{ id, topic, los, difficulty, vignette, options:{A,B,C}, answer, explanation:{A,B,C}, tag, keys? }
```

Add new weak-spot tags to `TAGS` and formula cards to `CARDS`.
