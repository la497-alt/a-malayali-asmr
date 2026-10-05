# A malayali ASMR

Type a name and watch it appear in Malayalam, written not in ink but in water condensing on a rainy window, over a Kerala river you can ripple with your hand. Rain and piano music are synthesized live in the browser, and each name sets its own weather and its own tune.

## How the lettering works

The name is never drawn. It emerges from thousands of drops following a few simple rules:

1. Rain lands anywhere on the glass. Mist gathers where the name was "traced."
2. Off the name, water evaporates. On the name, it clings and slowly swells.
3. Drops that touch merge into one, keeping their volume.
4. A drop too heavy for the glass slides down, leaving a beaded trail, until sticky glass stops it.
5. Dragging across the name wipes the glass; the pushed water piles up and runs.

Each new name condenses in about 3 seconds and holds still for 3 seconds so it can be read, then the beads are released one by one. These timings are `FORM`, `READ` and `EASE` in `index.html`.

## The rest of the piece

- **Rain intensity** comes from the Malayalam spelling: longer names, conjuncts and harder consonants bring heavier rain.
- **Music** is a public-domain piano melody chosen per name; the number of syllables sets how full it plays.
- **The river** is a WebGL ripple simulation. Only the water in each photo ripples, using an outline traced per photo (`river` in `index.html`).
- **Reduced motion:** with the system setting on, the name shows as still chalk lettering.

## Name conversion

Names are converted with a built-in list of common Kerala and international names, then Manglish spelling rules for anything not on the list. Names typed directly in Malayalam script are shown exactly as typed. If a spelling looks wrong, typing the name in Malayalam always works.

## Run it

No build step and no dependencies. It's a single `index.html` plus the `images` folder.

- **GitHub Pages:** in the repository settings, open Pages, choose "Deploy from a branch," select `main` and `/ (root)`, and save.
- **Locally:** run `python3 -m http.server` in this folder and open `http://localhost:8000`. Opening the file directly by double-clicking also works, but browsers block the river ripples on `file://` pages and show the still photos instead.

## Files

```
index.html     the whole piece: markup, styles, simulation, audio
images/        the three river photographs
```
