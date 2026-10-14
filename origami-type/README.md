# Origami Type

Live: https://type-experiments-cyan.vercel.app/origami-type

Letters built from paper triangles that unfold like folded paper.

## Run
Open `index.html` in a browser. No build step. Google Fonts load from the web.

## How it works
- Each letter is drawn to a hidden canvas, then covered with a jittered triangle mesh that follows the glyph shape.
- Neighbouring triangles share an edge. A breadth-first search from a random root gives every triangle a parent and a hinge, so the letter opens as a wave.
- A triangle folded by angle phi around its hinge is squeezed by cos(phi) across the hinge line. Each triangle's matrix is its parent's matrix times its own fold. Past 90 degrees you see the pale back of the paper.
- Backspace refolds the letter in reverse order. Space adds a zigzag paper ribbon under the finished word.

## Use
- Type, space, backspace, enter (clears).
- Pointer "fold": facets near the cursor curl up and shrink. Set it to "off" to disable.
- Speed slider changes the unfolding speed.
- Style: paper (palette gradient) or mono (one ink color).
- Symmetry: mirror horizontal or vertical, kaleidoscope 4 or 6.
- Export PNG or SVG (triangles as polygons, no font needed).

## Notes
- Folds compound down the hinge chain, so wobble must never touch the geometry (only shading), or the letter deforms.
- Max 40 characters to keep the frame rate high.

## Credits

Inspired by [Type Garden](https://type-garden.vercel.app/) by Akshat Agarwal.

Built by [Ariel Cerda](https://www.arielcerda.com/).
