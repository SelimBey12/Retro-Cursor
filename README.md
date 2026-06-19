# 🖱️ Retro Cursor with Base64

A dependency-free HTML/CSS/JavaScript demo that replaces the default mouse cursor with a custom **Base64**-encoded image, automatically swapping the cursor's appearance when hovering over a button.

## ✨ Features

- 🎨 The browser's default cursor is hidden and replaced with a custom image
- 🖱️ The cursor image follows mouse movement in real time
- 🔄 The cursor image automatically changes when hovering over a button (hover effect)
- 📦 All images are embedded as Base64 directly in the HTML/JS — no external files or internet connection required
- 🚫 No libraries or frameworks used (vanilla HTML/CSS/JS)

## 🚀 Usage

1. Download (or clone) the `index.html` file from this repo.
2. Open the file in any modern browser.
3. Move your mouse and hover over the button in the center to see the cursor change.

No installation, build step, or external dependency is required — just open a single HTML file.

## 🧠 How It Works

- The `cursor: none;` rule hides the browser's default cursor across the whole page (and the button).
- A fixed-position (`position: fixed`) `<img id="cursor">` element is added to the page.
- A `mousemove` event listener continuously updates this element's `left` / `top` position to match the mouse coordinates.
- `mouseenter` and `mouseleave` events are listened for on the button; when triggered, the cursor image's `src` is swapped between its normal and hover state.
- Both cursor images (`normalCursor`, `hoverCursor`) are embedded as `data:image/png;base64,...` strings directly in the JavaScript, so no separate image files are needed.

## 📁 File Structure

```
.
└── index.html   # Single file containing all HTML, CSS, and JavaScript
```

## 🎨 Customization

| What to change | Where |
|---|---|
| Cursor images | The Base64 data in the `normalCursor` and `hoverCursor` variables |
| Background color/gradient | The `background` property on the `body` selector |
| Button style (color, size, animation) | The `button` and `button:hover` CSS rules |
| Cursor size | The `width` / `height` values on the `#cursor` selector |

## 🌐 Browser Support

Works smoothly in all modern browsers (Chrome, Firefox, Edge, Safari). No polyfills or special configuration required.

## 📄 License

This project is free to use, modify, and distribute. (Feel free to update this section with a specific license, e.g. MIT.)
