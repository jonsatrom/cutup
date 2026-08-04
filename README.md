# CUT/UP

A William S. Burroughs cut-up machine. Paste text. Cut. Shake. Read. Repeat.

A single self-contained `index.html` — no build step, no dependencies. Open it in a browser, or serve the repo statically (`python3 -m http.server`), or point GitHub Pages at it.

## Methods

Three cuts, each drawn from accounts of Burroughs' and Brion Gysin's practice:

- **Strip cut** — the basic scissors-and-paste operation: the text is cut into slips of a few words each and rearranged.
- **Four-square page** — Gysin's original 1959 Beat Hotel accident: the page sliced into four quadrants with a Stanley blade, the sections rearranged, read straight across the new seams.
- **Fold-in** — the method of *The Ticket That Exploded*: one page folded down the middle and laid on another, splicing half-lines together. Takes an optional second text; with none given, the text is folded onto itself.

## The scissors

- **Cut size** — words per slip (1–12).
- **Ragged edge** — random variation in slip length (±0–6 words).
- **Shake radius** — how far a slip may drift from where it was cut: 0% keeps fragments near their neighbours, 100% scatters the whole page. (Strip cut only.)
- **Passes** — feed the result back through the scissors, up to 4 times.
- **Seed** — the cut is deterministic: the same seed always reproduces the same page. **Shake again** rolls a fresh seed.

## The voice

The machine can read the cut aloud (browser speech synthesis — no network, no accounts). The voice picker prefers the junkiest robot voices your device has installed (Zarvox, Fred, Albert…). **Speed** and **pitch** set the base delivery; **rust** lets every slip drift in pitch and speed — more rust, more broken machine, and the drift is seeded, so the same seed always breaks the same way.

Beneath the voice, an **underlayer** of synthesized sound: vowels become square-wave tones on a minor pentatonic scale, consonants become filtered noise, pitched by where each slip came from in the source (early text low, late text high), over a low tape-machine drone. Run it per word or per letter, or switch it off. The slip being spoken is highlighted on the table.

## Reading the table

The result lands as paper slips. Each slip's left edge is tinted by *provenance* — where the fragment came from in the source: red for the start of the text, blue for the end — tracked per word, so it stays honest across multiple passes. Toggle to a plain prose view, or copy the text out.

> "When you cut into the present the future leaks out." — W.S.B.
