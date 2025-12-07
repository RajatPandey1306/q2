---
marp: true
title: Marp — Never use PowerPoint again
author: 21f3001699@ds.study.iitm.ac.in
theme: default
paginate: true
---

<!--
  Presentation: Product Documentation (20 min)
  - Includes custom theme, page numbers, background slide,
    directives, and math equations as requested.
-->

<style>
section {
  background: linear-gradient(180deg,#ffffff,#f4f8ff);
  color: #0b2545;
  font-family: Inter, Arial, sans-serif;
}
h1, h2 { color: #0b4bd8; }
.lead { font-size: 1.45em; }
pre { background: #0f1724; color: #e6eef8; padding: 0.75rem; border-radius: 6px; }
code { background: rgba(11,66,216,0.06); padding: 0.15rem 0.35rem; border-radius: 3px; }
.meta { font-size: 0.85em; opacity: 0.85; }
</style>

---

<!-- _class: lead -->
# Marp — Never use PowerPoint again

**Author:** 21f3001699@ds.study.iitm.ac.in

_A quick guide to authoring product documentation presentations with Marp._

---

<!-- _footer: "21f3001699@ds.study.iitm.ac.in" -->
## Why Marp?

- **Plain-text:** Version-control friendly Markdown
- **Flexible exports:** HTML / PDF / PPTX / images
- **Theming & directives:** Consistent styling across decks
- **Great for technical content:** Code, math, diagrams

---

<!-- _backgroundColor: #0b4bd8 -->
<!-- _color: white -->
<!-- _class: lead -->
![bg cover](https://picsum.photos/1600/900)

# Visuals & Branding

Use background images for impact. The example uses a remote image; replace with a local file during exports:

`![bg cover](images/branding-bg.jpg)`

---

## Custom Theme Example

You can place CSS inside the Markdown deck to style slides, headings, and code blocks. The `<style>` block at the top is a minimal custom theme.

Example snippet:

```css
section { background: #f7fbff; }
h1 { color: #0b4bd8; }
```

---

## Math & Complexity

Block math is supported via KaTeX.

Inline: $E = mc^2$

Block example (algorithmic complexity):

$$
T(n) = \\\sum_{i=1}^{n} i = \\\frac{n(n+1)}{2} = O(n^2)
$$

Another useful form:

$$
T(n) = O(n \\\log n)
$$

---

## Code Example

```javascript
function quickSort(arr) {
  if (arr.length < 2) return arr;
  const pivot = arr[Math.floor(arr.length/2)];
  const left = arr.filter(x => x < pivot);
  const right = arr.filter(x => x > pivot);
  return [...quickSort(left), pivot, ...quickSort(right)];
}
```

---

## Exporting

- HTML: `marp slides.md -o slides.html`
- PDF: `marp slides.md --pdf --allow-local-files`
- PPTX: `marp slides.md --pptx`
- Images: `marp slides.md --images png`

If using local images in PDF export add `--allow-local-files`.

---

## File Organization (recommended)

```
presentation/
├── slides.md        # Main presentation (this file)
├── images/          # Images (branding-bg.jpg, diagrams)
├── themes/          # Optional custom theme files
└── package.json     # Build scripts (optional)
```

---

<!-- _footer: "Slides: Product Documentation — 21f3001699@ds.study.iitm.ac.in" -->
## Tips & Best Practices

- Keep slides focused and minimal
- Use code blocks for reproducible examples
- Test PDF and PPTX exports (fonts, images)
- Use `paginate: true` to show page numbers

---

## Next Steps

- Add your `images/branding-bg.jpg` for offline exports
- Optionally add a `package.json` with build scripts

---

**End** — Contact: 21f3001699@ds.study.iitm.ac.in