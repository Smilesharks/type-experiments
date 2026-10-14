# Ornament Type

Live: https://type-experiments-cyan.vercel.app/ornament-type

A typing toy. Every letter grows swashes, curls, tails, dots and diamonds that behave like ropes (springs, wind, gravity, pointer).

## Run
Open `index.html` in a browser. No build step. Google Fonts load from the web.

## Use
- Type: letters pop in and ornaments grow. Same word gives the same design.
- Space: finishes the word with a tail under it.
- Backspace: removes the last letter, its ornaments retract.
- Enter or Clear: clears everything.
- Pointer: push, pull or off. Move fast over letters to shake them.
- Calm slider: less wind, gravity and bounce. Ornaments never fully freeze.
- Symmetry: mirror horizontal, mirror vertical, kaleidoscope 4 or 6.
- Style: ink (one color) or filled (accent color with ink outline).
- Export: PNG, or SVG (letters as live text, ornaments as paths).

## Code map (all in index.html)
1 config, 2 math helpers, 3 rope shapes, 4 state, 5 layout, 6 ornament generator,
7 letters and physics, 8 symmetry, 9 update, 10 renderer, 11 input, 12 export, 13 UI, 14 start.

## Ideas for next steps
- Keep ornaments from overlapping the next line.
- Per-word color accents, more ornament types (stars, ribbons).
- Record a looping video of the sway.
