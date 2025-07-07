# 📂 KANLEP — Project Structure (README)

This document outlines the structure, styling, and implementation notes for the **KANLEP** poetic archive site: *Barking at Baxter's*.

---

## 🔸 Indexed Pages

### `index.html`
- Entry point to the site. A surreal poetic boot sequence introducing the Kanlep aesthetic.
- **CSS:** `style-home.css`
- **Fonts:** Courier Prime, Oswald, Space Grotesk
- **Main Classes:**
  - `.titulo-kanlep`
  - `.aparicion-ritual`
  - `.verso-ayma`
  - `.advertencia-kanlep`
  - `.fecha-kanlep`

---

### `repertorio.html`
- Acts as a poetic "library" linking to all `archivo-001.html` through `archivo-013.html`.
- **CSS:** `style-repertorio.css`
- **Background:** `/assets/backgrounds/repertorio-bg.png`
- **Layout:** Grid or list of archive links
- *Optional:* Wrap the list in a semi-transparent container for better legibility.

---

### `contacto-y-derechos.html`
- Legal and poetic disclaimer using a `<pre>` block for poetic formatting.
- **CSS:** `style-contacto.css`
- **Font:** Courier Prime
- **Background:** `/assets/backgrounds/licencia-bg.jpg`
- **Required Elements:**
  - `kanlep@outlook.es` (as visible email contact)
  - `barkingatbaxters.com` (as plain text hyperlink)

---

### `bio-de-kanlep.html`
- Silent full-screen page showing a single image.
- **Image Path:** `/assets/images/bio.png`
- *Optional:* Add a hidden tag inside `<body>` for accessibility or SEO.

---

## 🔸 Archivo Pages

### `archivo-001.html` to `archivo-013.html` (excluding `archivo-004.html`)
- Visual-only poem pages.
- **Image Source:** `/assets/images/archivo-00X.png`
- **Background:** `/assets/backgrounds/archivos-bg.png`
- **Navigation Arrows:**
  - Left: `/assets/nav/arrow-left.png`
  - Right: `/assets/nav/arrow-right.png`
- Each arrow links to the previous or next archive page.
- Position arrows using absolute or flexbox.
- No overlay text unless otherwise stated.

---

### `archivo-004.html`
- A unique poetic slide with animated line appearance.
- **CSS:** `style-archivo-004.css`
- **Font:** Courier New
- **Animation:** Fade-in blur from the bottom
- **HTML Structure Includes:**
  - Title: `Archivo #004`
  - Poetic text inside `.poesia-congelada`
- **Background:** `/assets/backgrounds/archivos-bg.png`

---

## 🔹 Template Navbar

The navigation bar must be included on all pages to maintain consistency and provide seamless user navigation.

### Files Required:
- `navbar.html` — HTML structure
- `style-navbar.css` — Styling (Courier New font, dark background)

### Placement:
- Paste `navbar.html` contents inside the `<body>` of each page (near the top).
- Link to `style-navbar.css` in the `<head>` of each HTML page.
- Nav links should point to:
  - `index.html`
  - `repertorio.html`
  - `bio-de-kanlep.html`
  - `contacto-y-derechos.html`

---

## 🔹 Template Archivo Pages

Used for `archivo-001.html` to `archivo-013.html` (excluding `archivo-004.html`).

### Instructions:
- Replace `<head>` with `template-head.txt` content.
- Update:
  - Page title
  - `meta name="robots"`
  - `og:url`
- Update the image source to `/assets/images/archivo-00X.png`
- Ensure `alt` text matches the archive number.
- Use unified background `/assets/backgrounds/archivos-bg.png`
- Use the navigation structure and styling described above.

---

## 🔸 404.html
- Custom poetic error page.
- **CSS:** `style-404.css`
- **Font:** Courier Prime
- Centered poetic message layout.
- Default poetic mood background.

---

## 🔹 Mobile Display Blocker (Planned)
- A mobile screen size blocker will be added based on viewport width (e.g., under 768px).
- Ensures the site is experienced only on properly sized screens.
- May use CSS media queries or JavaScript detection.
- Final decision on breakpoint pending.

---

## ✅ Directory Structure

- All assets live inside `/assets/`
  - Backgrounds → `/assets/backgrounds/`
  - Images → `/assets/images/`
  - Navigation icons → `/assets/nav/`
- CSS files go in the root directory

---


