# 🎂 Happy Birthday Celebration Page

A beautiful, animated birthday greeting page featuring a blooming tree with hearts, a typewriter message, and background music — all rendered on an HTML5 canvas.

---

## ✨ Demo

Open `index.html` in your browser (or serve it with a local HTTP server) to see:

1. 🌱 A seed on the canvas — **click it** to start the animation (and play the music).
2. 🌳 A tree grows branch by branch.
3. 💗 Blossoms bloom into hearts.
4. 💌 A personalised birthday message appears with a typewriter effect.

---

## 🚀 Features

- **Canvas animation** — hand-crafted Bézier-curve branches and heart-shaped blooms.
- **Typewriter effect** — birthday messages appear letter by letter.
- **Background music** — an audio clip plays when the seed is clicked.
- **Background image** — full-cover background (`img2.png`) sets the mood.
- **Zero dependencies to install** — all libraries (`jQuery`, `Jscex`) are bundled locally in `file/`.

---

## 📁 File Structure

```
hbd/
├── index.html          # Entry point — boots the animation & defines opts
├── aud.mp3             # Background birthday music
├── img2.png            # Full-cover background image
└── file/
    ├── default.css                    # Styles for layout and text
    ├── love.js                        # Core animation: Tree, Branch, Bloom, Seed
    ├── functions.js                   # Helpers: typewriter plugin, timeElapse
    ├── jquery.min.js                  # jQuery (bundled)
    ├── jscex.min.js                   # Jscex async transpiler (bundled)
    ├── jscex-parser.js
    ├── jscex-jit.js
    ├── jscex-builderbase.min.js
    ├── jscex-async.min.js
    └── jscex-async-powerpack.min.js
```

---

## 🛠️ Running Locally

### Option 1 — Open directly
Double-click `index.html` in your file manager and open it with Chrome or Firefox.

> **Note:** Some browsers block audio autoplay on `file://` URLs. Use Option 2 to avoid this.

### Option 2 — Local HTTP server (recommended)

```bash
# Python 3
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in your browser.

---

## 🎨 Customisation

### Change the birthday message
Edit the `<span class="say">` lines in `index.html`:

```html
<span class="say">Your custom message here 🎉</span><br />
```

### Change the background music
Replace `aud.mp3` with your own MP3 file (keep the same filename, or update the `src` attribute in `index.html`).

### Change the background image
Replace `img2.png` with your own image, or update the `background-image` path in `file/default.css`:

```css
background-image: url('../your-image.png');
```

### Adjust the tree / bloom
Tweak the `opts` object inside the `<script>` block at the bottom of `index.html`:

| Property | What it controls |
|---|---|
| `opts.seed.color` | Colour of the seed / heart |
| `opts.bloom.num` | Number of heart blossoms |
| `opts.branch` | Branch coordinates (Bézier control points) |
| `opts.footer` | Footer line dimensions and speed |

---

## 🧰 Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 Canvas | Drawing the tree, branches, and blossoms |
| JavaScript (ES5) | Animation logic |
| [jQuery](https://jquery.com/) | DOM helpers & event handling |
| [Jscex](https://github.com/JeffreyZhao/jscex) | Async animation sequencing |
| CSS3 | Layout and text styling |

---

## 📜 License

This project is open-source and free to use for personal birthday greetings. 🎁
