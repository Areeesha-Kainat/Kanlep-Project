🟣 KANLEP — PROJECT STRUCTURE README.txt

This README contains notes and instructions for the pages and CSS files included in the Barking at Baxter's poetic terminal.

The indexed pages are: index.html, repertorio.html, contacto-y-derechos.html

---

🔷 index.html
Main entry point. Styled with `style-home.css`.
- Fonts: Courier Prime, Oswald, Space Grotesk
- Elements: `.titulo-kanlep`, `.aparicion-ritual`, `.verso-ayma`, `.advertencia-kanlep`, `.fecha-kanlep`
- Purpose: A surreal poetic boot sequence; introduction to the Kanlep aesthetic.

📎 style-home.css → controls all layout, fonts, and animations for index.html.

---

 bio.html
A silent page featuring a single image background: `/assets/images/bio.png`
- No visible content on screen.
- Add the following hidden tag inside the `<body>`:


---

🔷 🔷 contacto-y-derechos.html
Legal + poetic disclaimer. Uses a styled <pre> block.

📎 style-contacto.css → applies background image, formatting, shadows, etc.

Background image: /assets/backgrounds/licencia-bg.jpg

Font: Courier Prime

Format: center-aligned <pre> with poetic/legal text

Purpose: Licenses, warnings, contact, and legal language presented with mystique.

➤ Must include two hyperlinks inside the <pre> block:

kanlep@outlook.es (as a visible email contact)

barkingatbaxters.com (as a text hyperlink, not a button)

---

Revised version of the first block:
🔷 archivo-001.html → archivo-013.html (except archivo-004.html)
Thirteen poetic pieces delivered as standalone image pages.
Note: archivo-004.html uses a different structure and is described separately below.

Each applicable HTML should contain a single <img> tag pointing to:
/assets/images/archivo-00X.png

Each page must use a unified background:
/assets/backgrounds/archivos-bg.png

Navigation is provided via black arrow icons placed on each side of the image:

Left arrow → link to previous archivo-00X.html

Right arrow → link to next archivo-00X.html

Arrows are image files in: /assets/nav/arrow-left.png and /assets/nav/arrow-right.png

Hyperlinks are wrapped around the arrows. They should be positioned with absolute or flexbox to allow click navigation without visible button frames.

No inner text or overlay unless specifically noted. These are purely visual poems.



---

🔷 archivo-004.html
Standalone poetic slide. Minimal HTML, styled directly via style-archivo-004.css.

📎 style-archivo-004.css → animation and styling for the appearance of the poetic line.

Font: Courier New

Animation: fade-in blur from bottom

Class: .poesia-congelada

HTML structure:

<div class="titulo-archivo">Archivo #004</div>
<div class="poesia-congelada">
  ella es hielo<br><br>
  hielo de helio
</div>
Background image path: /assets/backgrounds/archivos-bg.png

---

🔷 repertorio.html
Index page listing all 13 poetic image-archives with links.

Background image: /assets/backgrounds/repertorio-bg.png

Lists or grid of links: archivo-001.html → archivo-013.html

Styling via style-repertorio.css

Purpose: Acts as the “library” or map of the project

📝 Note: We may need to wrap the link list in a semi-transparent container (div) to improve legibility over the background.

---

🔷 404.html
Custom error page served when a user lands on a missing or invalid URL.
Styled with style-404.css.

📎 style-404.css → applies typographic styling and visual mood consistent with the site’s tone.

Typography: Courier Prime

Layout: centered message, poetic structure

Default background image.

---


📎 TEMPLATE COMPONENTS:

🔹 Template HEAD
Use the current <head> block (from template-head.txt) on all pages.
For indexed pages (index.html, contacto-y-derechos.html, repertorio.html), leave this line as is:

<meta name="robots" content="index, follow">

For non-indexed pages, change it to:

<meta name="robots" content="noindex, nofollow">

Please also update the og:url on each page to match its full live URL — especially if pages will be shared individually.

---

🔹 Template NAVBAR

Included in ALL pages
Composed of two files:
	-navbar.html — HTML block with navigation structure
	-style-navbar.css — Styles (Courier New font, black background, centered links)
Implementation:
Copy the contents of navbar.html and insert it inside the <body> of each page.
Include the stylesheet in the <head> of each page:

<link rel="stylesheet" href="style-navbar.css">

Links should point to:
index.html
repertorio.html
bio.html
contacto-y-derechos.html

---



🔷 template-archivo_001-13.html

This file is included as a base template to generate the twelve archivo-001.html → archivo-013.html pages.
Note: archivo-004.html is handled separately, as it follows a different structure and styling (see section on archivo-004.html above).

Instructions:

Replace the <head> section with the full contents of template-head.txt.

Update the <title>, <meta name="robots">, and (optionally) og:url per page.

In the <body>, update the <img src> and alt attribute to reflect the correct image file:

<img src="/assets/images/archivo-00X.png" alt="archivo 00X" />

Background and layout styles are already embedded via <style>.

Each final page should show one centered poem image on the unified background:
/assets/backgrounds/archivos-bg.png

---

📎 OTHER:

🔷 Mobile Display Blocker (pending implementation)

The project will include a mobile screen size blocker, not based on operating system, but on viewport width (inches or pixels).

This ensures poetic content is only experienced on screens large enough to carry the full mood and typographic layout.

Implementation will likely use a CSS media query or JavaScript detection targeting viewports under ~768px width.

Final decision on exact breakpoint (in px or equivalent inch approximation) pending discussion.


---

✅ Directory expectations:
- All assets (images, icons, backgrounds) go into `/assets/`
- Backgrounds specifically: `/assets/backgrounds/`
- Poem images: `/assets/images/`
- Navigation icons: `/assets/nav/`
- CSS: in the root

---

Let me know if something breaks. Or don't. This site isn't exactly built for safety.
