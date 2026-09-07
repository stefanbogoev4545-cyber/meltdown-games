# Game Studio — state as of 2026-09-04

## Flagship: MELTDOWN
`meltdown\index.html` — double-click to play. Backup: `builds\meltdown-v4-2026-09-04.html`

One-tap timing game wrapped in press-your-luck psychology. Reactor theme (deliberately
NOT casino imagery — Poki/CrazyGames restrict gambling-styled content for teen audiences).

### Built
- **Core loop** — pointer sweeps a ring, tap to stop it in the hot zone. Each hit raises
  the output multiplier, shrinks the window, speeds the sweep.
- **5 zones**, every 6 injections, each with different pointer behaviour:
  CORE (steady) · FLUX (speed breathes) · SURGE (polarity flips) ·
  PHANTOM (window goes invisible) · OVERDRIVE (stutter between half and double speed)
- **Obstacles** — red breach arcs on the ring, instant death, 0-3 by zone. Never placed
  overlapping the target, so a hit is always physically possible.
- **Boss: PRESSURE LOCK** every 12 injections. Hold to raise a needle, release inside a
  moving green band. 3 locks needed, 5 failures ends the run. Clear = output x2 + 1 core.
- **3 modes** — SOLO (safe banking, continues allowed) · CREW (ghosts, winner-takes-all)
  · DAILY (seeded from the date, identical run for everyone, resets at midnight)
- **Ghost operators** (CREW) — 4 recorded runs sampled from a local pool. They eject or
  melt at their recorded depth while you watch. Melted operators hand you 60% of their
  output as salvage. Outlast all four for a compounding SOLO +25% bonus.
- **Winner takes the pot** (CREW) — ejecting only submits a score. Highest output among
  all five takes everything; everyone else gets nothing.
- **Continue** (SOLO/DAILY only) — ad placeholder or cores, cost rises 1/2/3 per run.
- **Economy** — CREDITS (earned) and CORES (premium: nothing before depth 12, scaling
  chance after, guaranteed at depth 22, always from bosses).
- **8 skins** — EMBER free / VOID 25k / CHROME 100k / TOXIC 250k / ABYSS 500k /
  NOVA 3 cores / SINGULARITY 8 cores / AURUM licence-only.
- **OPERATOR LICENCE** $4.99 — the real-money product. 1 free continue per run,
  +25% banked forever, 1 core daily, AURUM skin. Compounding value, not a consumable.
- Menu particles, 16 distinct synthesized sounds, pause with 3-2-1 resume countdown,
  records screen.

### Not built (needs infrastructure, not code)
- **Real payments** — store buttons are deliberately dead and labelled. Needs a payment
  provider + server.
- **Real ads** — the continue flow works against a labelled 5s placeholder. An ad SDK
  (Poki, CrazyGames, AdSense H5) drops into that exact spot.
- **True multiplayer** — CREW is asynchronous by design. When hosted, the ghost pool
  fills with real players' runs and it becomes genuinely multiplayer with no rewrite.

### Open questions for Stef
1. Does the PRESSURE LOCK boss feel good? Designed blind, most likely thing to be wrong.
2. Are obstacles fair or cheap, especially in PHANTOM where the window hides?
3. Are cores too hard to earn? Depth 12 is a hard wall right now.
4. Does winner-takes-all make CREW tense or just frustrating?

## Other games
- `nerve\index.html` — the pre-reactor prototype MELTDOWN grew out of. Superseded.
- `locked-in-stack\index.html` — game #1, Ketchapp-style one-tap stacker. Complete and
  shippable; kept as a portfolio piece.

## Next steps
1. Tune from Stef's feedback on the four questions above.
2. Ship to CrazyGames + GameMonetize (web form upload, zip with index.html at root).
3. Cut Shorts/TikTok clips — PHANTOM near-misses and winner-takes-all losses are the
   best material. Separate channel from the love-edits one.
