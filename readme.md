# Food Corner
# Live Link: cheery-zabaione-c11720.netlify.app

A single-page restaurant website built with plain HTML, CSS and a little JavaScript for **Web Technologies, Lab 3 (CSS)** at COMSATS University Islamabad, Wah Campus.

The design is minimal: black, white and whitesmoke, with one green accent (`#2f5d3a`).

## Project structure

```
FoodCorner/
├── index.html      Page structure, internal CSS, inline CSS and JavaScript
├── style.css       External stylesheet (all main styling)
├── README.md
└── images/
    ├── pizza.svg
    ├── burger.svg
    ├── sandwich.svg
    └── pasta.svg
```

## How to run

1. Download or unzip the `FoodCorner` folder.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).

No installation, build step or internet connection is needed.

## Features

- **Header and navigation:** sticky header, hover effects, and the link for the section you are viewing is highlighted.
- **Welcome section:** heading, short paragraph and an Explore Menu button.
- **Menu cards (Pizza, Burger, Sandwich, Pasta):** each has an image, name, description, price and Order Now button.
  - Order Now becomes a quantity stepper (`−` / `+`).
  - The Your order button in the header shows the item count and opens a summary with the total. Press `Esc` to close it.
  - A **Show box model** toggle highlights each card's margin, border, padding and content.
- **About section:** restaurant description plus three live CSS demos (margin collapsing, width/height limits, overflow).
- **Contact form:** Name, Email, Message and Submit, with inline validation. It does not send data anywhere.
- **Footer:** © 2026 Food Corner.

## Lab requirements and where to find them

| Requirement | Where |
|---|---|
| Inline CSS | `style` attribute on the hero paragraph and the `<footer>` in `index.html` |
| Internal CSS | `<style>` block in `<head>` of `index.html` (`#home` hero background) |
| External CSS | `style.css`, linked in `<head>` |
| Element selector | `body`, `a`, `section`, `footer` |
| Class selector | `.card`, `.btn`, `.panel` |
| ID selector | `#home`, `#hint`, `#form` |
| Attribute selector | `input[type="checkbox"]`, `input[type="text"]`, `input[type="email"]` |
| Grouping selector | `h1, h2, h3`, `body, h1, h2, h3, p, ul` |
| Descendant selector | `.card .price`, `.card .desc`, `nav a` |
| `:hover` | Nav links, `.btn`, cart button, cards |
| `:first-child` | `.card:first-child` (dark card) |
| `::before` / `::after` | `.section-title::before` and `::after`, plus the "Most loved" badge on the first card |
| Inheritance | Font and colour set on `body`; `font: inherit` override on form controls |
| Specificity | `#hint` beats `.panel .hint`; `#home` beats `section` |
| Cascade / source order | Two `.tag` rules with equal specificity; the later one wins |
| Fonts, text | `font-family`, `font-size`, `font-weight`, `font-style` (italic on `.lead`), `text-align`, `text-decoration`, `line-height` |
| Colours | Named (`black`, `whitesmoke`, `crimson`), HEX (`#2f5d3a`), RGB (`rgb(95, 95, 95)`) |
| Background | `background-color`, `-image`, `-repeat`, `-position`, `-size` on `#home` |
| Box model | `.card`: `width`, `height`, `padding`, `border`, `margin`, `box-sizing: border-box` |
| Margin collapsing | `.mc-a` (bottom 40px) and `.mc-b` (top 24px): the gap is 40px, not 64px |
| Width/height constraints | `.size-box`: `width`, `height`, `min-*`, `max-*` |
| Overflow | `.ov` switches between `visible`, `hidden` and `scroll` |

## Margin collapsing, briefly (for the report)

When the bottom margin of one block meets the top margin of the next block, the two margins combine into one. The gap is the larger of the two, not their sum. Here, 40px and 24px give a 40px gap. Margins do not collapse in flex or grid layouts, which the **Prevent collapsing** button demonstrates.

## Customising

- **Colours:** edit the variables at the top of `style.css` (`:root`).
- **Menu items:** change the `data-name` and `data-price` attributes on each `.card` in `index.html`, along with the visible text.
- **Images:** replace the files in `images/` or change the `src` paths in `index.html`.