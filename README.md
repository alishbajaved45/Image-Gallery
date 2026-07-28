# Image Gallery

A fully responsive, premium-styled image gallery built from scratch using **vanilla HTML, CSS, and JavaScript**  no frameworks, no external libraries.

This project focuses on core front-end fundamentals: layout systems, DOM manipulation, and interaction design, without leaning on a framework to handle state or rendering.

---

## 🔗 Live Preview

Open `image-gallery.html` directly in any browser. It's a single self-contained file — no build step, no dependencies required.

---

## ✨ Features

| Feature | Details |
|---|---|
| **Responsive CSS Grid** | 3 columns on desktop, 2 on tablet, 1 on mobile — fluid at every breakpoint |
| **Category filters** | All / Landscape / Architecture / Portrait / Street, filtered live on the client side |
| **Lightbox viewer** | Click any image to open a fullscreen view with a blurred backdrop |
| **Next / Previous navigation** | On-screen buttons *and* ← → arrow key support |
| **Keyboard accessibility** | Enter/Space to open a card, Esc to close the lightbox, visible focus states throughout |
| **Hover micro-interactions** | Card lift, image zoom, and shadow transitions on a smooth 0.3s ease curve |
| **Reduced-motion support** | Respects `prefers-reduced-motion` for users who need it |

---

## 🛠️ Built With

- **HTML5** — semantic structure
- **CSS3** — Grid, Flexbox, custom properties, `backdrop-filter`
- **Vanilla JavaScript** — DOM APIs only, no libraries

---

## 📁 Project Structure

```
CodeAlpha_ImageGallery/
├── image-gallery.html   # Complete project — markup, styles, and logic in one file
└── README.md
```

---

## 🎯 How It Works

1. Image data (source, category, caption) lives in a single JS array.
2. The grid is rendered dynamically from that array on page load.
3. Clicking a filter button toggles a `.hide` class on non-matching cards — no re-render needed.
4. Clicking a card opens the lightbox, tracking the current index **within the active filtered set** (not the full list).
5. Next/Prev buttons and arrow keys cycle through that same filtered set, with a fade transition between images.

This keeps the filtering and the lightbox in sync — browsing "Landscape only," for example, only cycles through landscape images in the viewer too.

---

## 📌 Note on Images

Images are pulled from [picsum.photos](https://picsum.photos) as placeholders. To use your own:

1. Open `image-gallery.html` and find the `photos` array in the `<script>` section.
2. Replace each `seed` value (or point `thumb` / `full` directly at your own image URLs).
3. Update the `cat` and `caption` fields to match.

No other code changes are needed — the grid and lightbox both read from this array automatically.

---

## 📚 What I Learned

Building this without a framework meant handling state manually tracking the active category filter and the current lightbox index, and keeping both in sync as the user interacts with the page. It was a useful exercise in writing clean, maintainable vanilla JS before reaching for a library to do it for me.

---

*Built as part of the CodeAlpha Web Development Internship  Task 1: Image Gallery.*
