# Shape Type

Live: https://type-experiments-cyan.vercel.app/shape-type

An original geometric alphabet built in code from simple shapes: rectangles, circles, half discs, quarter discs and triangles. No font file needed (only DM Mono for the interface).

## Run
Open `index.html` in a browser. No build step.

## How it works
- `ALPHA` (section 3) defines every glyph as a list of shapes in a unit box. Each shape has a color role (0, 1 or 2).
- A role maps to a palette color. Each letter rotates which palette colors it uses, so neighbours differ.
- Every shape arrives on its own: `slide` (from the sides or top), `spin` (turns and grows) or `drop` (falls and bounces).
- Space adds a border of small triangles, circles, half discs and squares under the finished word.
- Backspace plays the arrival in reverse. Enter clears.
- Pointer "twist": tiles near the cursor rotate like a revolving door.

## Use
- Style: color (palette) or mono (one ink color).
- Symmetry: mirror horizontal or vertical, kaleidoscope 4 or 6.
- Export PNG or SVG (every shape is a polygon, no font needed).

## Edit a letter
Open section 3 and change the shapes. Example: `def('A', 1, [Tr(0, 1, .5, 0, 1, 1, 0), Tr(.34, 1, .5, .6, .66, 1, 2)])`
- `R(x, y, w, h, role)` rectangle, `Ci(cx, cy, r, role)` circle
- `Hd(cx, cy, r, side, role)` half disc, `side` is where the curve bulges (t, b, l, r)
- `Qd(x, y, r, quad, role)` quarter disc, corner at (x, y), `quad` is br, bl, tl or tr
- `Tr(x1, y1, x2, y2, x3, y3, role)` triangle, `Pg([x, y, ...], role)` any polygon

Letters A to Z, digits 0 to 9 and . ! ? - are defined. Accented letters use their base letter. Anything else shows a small circle.

## Credits

Inspired by [Type Garden](https://type-garden.vercel.app/) by Akshat Agarwal.

Built by [Ariel Cerda](https://www.arielcerda.com/).
