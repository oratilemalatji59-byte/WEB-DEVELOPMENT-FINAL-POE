# WEB-DEVELOPMENT-FINAL-POE
FINAL CREATION OF GLAZE LIPGLOSS WEBSITE
# Glaze – Lip Gloss Website

Glaze is a small, animated website for a fictional lip gloss brand, built with plain **HTML, CSS and JavaScript**. There are no frameworks, no build step and nothing to install.

## Pages

| File | What it is |
|---|---|
| `home.html` | Landing page with a shade picker, typing headline and a "Say hello" welcome button |
| `shop.html` | Six shades with filter buttons (All, Sheer, Tinted, Clear) |
| `product.html` | Details for one gloss, with a quantity selector and "Add to bag" |
| `about.html` | The brand story and three brand values |
| `delivery.html` | Delivery options table and a delivery time estimator |
| `contact.html` | Contact form that shows a personalised thank-you message |

Each file contains its own CSS (inside `<style>`) and JavaScript (inside `<script>`), so every page works on its own.

## How to run

1. Put all six `.html` files in the same folder.
2. Double-click `home.html` to open it in any modern browser (Chrome, Edge, Firefox, Safari).
3. Use the menu at the top to move between pages.

Keep the file names exactly as they are. The pages link to each other by name.

An internet connection is needed the first time so the Google Fonts (Young Serif and DM Sans) can load. Without it, the site still works using fallback fonts.

## Features

**Moving parts**
- Floating glossy bubbles in the colour of the selected shade. They move away from your cursor, and clicking makes a burst of bubbles.
- A typing headline on the Home page that cycles through "stick", "drag", "fuss" and "flake".
- A gloss drop that bobs up and down and tilts to follow your mouse.
- The Home hero cycles through the shades by itself until you pick one.
- A scrolling ribbon under the header.
- Content that fades in as you scroll, shop cards that pop in one by one, and a shine that sweeps across buttons.
- A **Pause motion** button in the header stops all movement, and **Play motion** starts it again.

**Shopping**
- Filter the shop by finish.
- Clicking a gloss opens `product.html?id=…`, which reads the number in the address to show the right shade.
- The bag counter is saved in the browser (`localStorage`), so it stays when you move between pages.

**Forms and buttons**
- The welcome button on the Home page shows a welcome message.
- The contact form blocks the page reload, reads the name, shows "Thank you, *name*! Your message has been received." and clears the form.

**Design**
- Works on phones and desktops.
- Switches automatically to a dark theme when the device is in dark mode.

## Project structure

```
glaze-inline/
├── home.html
├── shop.html
├── product.html
├── about.html
├── delivery.html
├── contact.html
└── README.md
```

## Customising

- **Shades, prices and descriptions:** edit the `P` array near the top of the `<script>` in each page. Change it in every file so they match.
- **Colours:** change the variables at the top of the `<style>` section (`--bg`, `--ink`, `--accent` and so on). Dark-mode colours are in the `prefers-color-scheme: dark` block.
- **Delivery times and prices:** edit the table in `delivery.html`, and the province values in its `<select>` for the estimator.
- **Bubble count and speed:** in the script, look for `Array.from({length:34}` (how many) and the `mk` function (size, speed, opacity).
- **Turn off motion by default:** set `const reduce=false;` to `true` in the script.

## Good to know

- The content is placeholder: shades, prices (in Rand), brand story and delivery terms are made up.
- It is a front-end demo. The contact form does not send the message anywhere, and "Add to bag" only changes the counter. There is no checkout or payment.
- Because the CSS and JavaScript are repeated in each file, a design change needs to be made in all six files.
- The earlier version in `glaze-site/` splits the same code into separate `style.css` and `script.js` files, which is easier to maintain. It does not include the Contact page or the pause button.

## Credits

Made for the Glaze brand project. Fonts: [Young Serif](https://fonts.google.com/specimen/Young+Serif) and [DM Sans](https://fonts.google.com/specimen/DM+Sans) from Google Fonts.
