[README.md](https://github.com/user-attachments/files/29105433/README.md)
# Creato Creative Agency — Website

A single-page website for **Creato Creative Agency**, a graphic design studio based in Tagum City, Davao del Norte, Philippines. Built with plain HTML, CSS, and vanilla JavaScript — no frameworks, no dependencies beyond Google Fonts.

---

## 📁 File Structure

```
creato-website/
├── index.html        ← Main HTML file (all pages + JavaScript)
├── style.css         ← All styles, separated from the HTML
└── README.md         ← This file
```

---

## 🚀 How to Run

No build tools or server needed.

1. Download or clone the three files into the same folder.
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
3. That's it — the site runs entirely in the browser.

> **Tip:** If you want to edit and preview live, open the folder in VS Code and use the **Live Server** extension.

---

## 🗂️ Pages & Navigation

The site uses a **horizontal slide animation** — all 8 "pages" live in one HTML file and slide left/right like a carousel when you click the nav links or internal buttons.

| # | Page | How to reach it |
|---|------|-----------------|
| 0 | **Home** | Nav → Home |
| 1 | **About Us** | Nav → About Us |
| 2 | **Our Works** | Nav → Our Works |
| 3 | **Services** | Nav → Services |
| 4 | **Logo Design Pricing** | Services → Logo Designing → See Details |
| 5 | **Printables Pricing** | Services → Printables → See Details |
| 6 | **Digital Design Pricing** | Services → Digital Design → See Details |
| 7 | **Brief / Contact Form** | Logo Pricing → any package → Select |

---

## 📄 Page Details

### Home
- Headline in **Poppins Medium**
- "Creating New Heights" subline in **Montserrat Regular**
- **Contact Us** button links directly to the agency's Facebook page

### About Us
- Agency description in **Montserrat Regular**
- Accomplishments stats: **80+ Businesses**, **90+ Successful Projects**, **132 Total Clients**
- Closing tagline: *"We Help Brands & Businesses to Grow and we work with passion"*

### Our Works
- 6 project category cards with 2D minimalist SVG icons:
  Brand Identity, Print Collateral, Social Media, Logo Design, Packaging, Web Design

### Services
- 4 service cards: **Logo Designing**, **Printables**, **Digital Design**, **Brand Identity**
- Logo Designing and Printables → **See Details** button leads to pricing pages
- Digital Design → **See Details** button leads to digital pricing
- Brand Identity → **Coming Soon** badge

### Logo Design Pricing (Page 4)
Three packages with full feature lists:

| Package | Badge | Price |
|---------|-------|-------|
| Basic | Starter | ₱4,000 |
| Standard | Most Popular | ₱8,000 |
| Premium | Full Suite | ₱12,000 |

Each card has a **Select** button that carries the chosen plan into the Brief Form.

### Printables Pricing (Page 5)
Five item cards with peso pricing in green:

| Item | Pricing |
|------|---------|
| Menu | ₱599 – ₱2,500 (1–12 pages) |
| Packaging | ₱899 – ₱2,000 |
| Signage | ₱599 per design |
| Poster | ₱500 – ₱2,300 (1–12 pages) |
| T-Shirt | Sublimation ₱1,000 / DTF ₱899 |

### Digital Design Pricing (Page 6)
Three card types — Social Media, E-Commerce, Advertisement — each with the same poster bundle pricing:

| Bundle | Price |
|--------|-------|
| 4 Posters | ₱1,200 |
| 6 Posters | ₱1,600 |
| 8 Posters | ₱1,800 |

### Brief / Contact Form (Page 7)
Fill-up form fields:
- **Name**
- **Gmail**
- **Brand / Business Name**
- **What's Your Brand/Business?**
- **Preferences** (e.g. minimalist, modern, luxury)
- **Select Preferred Color** — preset swatches + custom color picker

On **Submit Brief**, the browser opens the user's Gmail `mailto:` with the full brief pre-filled, addressed to `eltonjohnganura@gmail.com`.

---

## 🎨 Design Tokens

| Token | Value | Used for |
|-------|-------|----------|
| Primary Green | `#00e633` | Buttons, accents, footer background |
| Dark Green | `#00b825` | Prices, eyebrows, stat numbers |
| Icon Green | `#00a820` | SVG icon strokes |
| Background | `radial-gradient(ellipse at top left, #b3ffb3 0%, #e6ffe6 30%, #fff 65%)` | Full-page background |
| Text | `#0a0a0a` | Body copy |
| Card border | `rgba(0,230,51,0.28)` | All cards |

---

## 🔤 Fonts

Both fonts are loaded from **Google Fonts** via `<link>` in the `<head>`.

| Font | Weight(s) | Used for |
|------|-----------|----------|
| **Poppins** | 500 (Medium) | Hero headline, page titles, card titles, stat numbers |
| **Montserrat** | 100, 400, 600, 700 | Nav links, body text, buttons, labels, footer |

Nav links use **Montserrat Thin (100)** by default and switch to **Bold (700)** when active/selected.

---

## ✉️ Contact & Social

| Channel | Details |
|---------|---------|
| Gmail | creatographic@gmail.com |
| Facebook | [Creato](https://www.facebook.com/profile.php?id=100082854266737) |
| Brief submissions sent to | eltonjohnganura@gmail.com |

---

## 🛠️ Customisation

### Change a price
Open `index.html`, search for the price (e.g. `₱4,000`) and update the number directly.

### Add a new nav page
1. Add a new `<div class="page">` block inside `.pages`
2. Increase the `width: 800%` on `.pages` and `calc(100% / 8)` on `.page` to match the new total (e.g. 9 pages → `900%` and `calc(100% / 9)`)
3. Update `const TOTAL = 8;` in the `<script>` to the new count
4. Add a `<a data-page="N">` link in the `<nav>`

### Change the slide animation speed / easing
In `style.css`, find:
```css
.pages {
  transition: transform 0.55s cubic-bezier(0.77, 0, 0.175, 1);
}
```
Adjust `0.55s` for speed or swap the cubic-bezier for a different easing curve.

### Update the brief recipient email
In `index.html`, find:
```js
window.location.href = 'mailto:eltonjohnganura@gmail.com?subject=...'
```
Replace the email address as needed.

---

## 📱 Responsive Behaviour

| Breakpoint | Layout changes |
|------------|---------------|
| ≤ 1000px | Tier grid → 2 columns; Print grid → 3 columns |
| ≤ 760px | Nav centers; pages padding reduced; most grids → 1–2 columns |
| ≤ 480px | All grids collapse to 1 column |

---

## 📜 License

All content, pricing, and branding belong to **Creato Creative Agency**. Code structure is freely reusable.
