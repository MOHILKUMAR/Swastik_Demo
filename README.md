# Swastik Hospital, Agra — One-Page Website

A fast, mobile-first, bilingual (English + Hindi) landing page for **Swastik Hospital**, a 24-hour maternity, gynaecology and critical-care hospital in Kaveri Vihar, Agra.

**Live site:** https://mohilkumar.github.io/Swastik_Demo/

The whole site is a single `index.html` file: no frameworks, no build step, no dependencies to install.

---

## Highlights

- **One file, zero build** – HTML, CSS and JavaScript all live in `index.html`. Open it in a browser and it works.
- **Mobile-first and responsive** – layouts adapt from large desktops down to small phones, with a collapsible menu and a floating "Call now" button on mobile.
- **Bilingual** – English content with Hindi (Devanagari) labels for the hospital name, services and doctors, using the *Tiro Devanagari Hindi* font.
- **Built to get patients in touch** – tap-to-call phone numbers everywhere, a 24-hour emergency bar, one-tap Google Maps directions and an embedded map.
- **Photo gallery with lightbox** – filter photos by *All / Outside / Inside*, open them full-screen, and move through them with the on-screen buttons or the arrow keys; `Esc` closes.
- **Accessible** – semantic sections, ARIA labels on the menu, gallery and lightbox, visible focus outlines, and support for `prefers-reduced-motion`.
- **SEO ready** – meta description, Open Graph tags for link previews, and `schema.org/Hospital` structured data (address, phone, geo-location, opening hours, specialties).
- **Graceful fallbacks** – if a hotlinked photo fails to load, a tinted placeholder is shown instead of a broken-image icon.

## Page sections

| Section | What it shows |
|---|---|
| Top bar | 24-hour emergency notice (English + Hindi) and both phone numbers |
| Hero | Hospital name, tagline, Google rating, call and directions buttons, building photo |
| Highlights | 24-hour deliveries, painless delivery, critical care, easy access |
| About | The hospital, the doctor couple who run it, and facilities |
| Services | Normal & caesarean delivery, painless delivery, CTG/NST monitoring, ultrasound, gynaecology & laparoscopy, infertility care, critical care, anaesthesia & pain relief, general medicine |
| Doctors | Dr. Vandana Jain (Obstetrics & Gynaecology) and Dr. Ankit Jain (Anaesthesia & Critical Care) |
| Gallery | Filterable photo grid with a full-screen viewer |
| Reviews | Google rating summary, common review themes, selected patient reviews |
| Contact | Address, phone numbers, hours, directions and an embedded Google Map |
| Footer | Quick links and contact details |

## Tech stack

- **HTML5** – semantic markup and JSON-LD structured data
- **CSS3** – custom properties (design tokens), CSS Grid and Flexbox, media queries
- **Vanilla JavaScript** – gallery filters, lightbox, mobile menu
- **Google Fonts** – *Newsreader* (headings), *Hind* (body), *Tiro Devanagari Hindi* (Hindi text)
- **Google Maps** – embedded map and directions links
- **GitHub Pages** – hosting

## Run it locally

No install needed.

```bash
git clone https://github.com/MOHILKUMAR/Swastik_Demo.git
cd Swastik_Demo
```

Then either open `index.html` directly in your browser, or serve the folder (recommended, so everything behaves as it does online):

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

The site is deployed with **GitHub Pages** from the `main` branch (root folder). Every push to `main` updates the live site automatically within a minute or two.

To set it up on a fork: **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save**.

## Editing the content

Everything is in `index.html`:

- **Colours and fonts** – the `:root` block at the top of the `<style>` section (`--blue`, `--red`, `--font-display`, etc.).
- **Phone numbers** – search for `tel:+91` and update every match (top bar, header, hero, contact, footer and the floating call button).
- **Services, doctors, reviews** – edit the matching `<section id="...">` blocks (`services`, `doctors`, `reviews`).
- **Gallery photos** – edit the `photos` array in the script near the bottom of the file. Each entry has an image `id`, a caption (`cap`) and a category (`cat`: `inside` or `outside`).
- **Search / social preview** – the `<meta>` tags and the `application/ld+json` block in the `<head>`.

## Project structure

```
Swastik_Demo/
├── index.html   # the complete website (markup, styles and scripts)
├── README.md    # this file
├── LICENSE      # MIT licence for the code
└── .gitignore
```

## Hospital details

**Swastik Hospital** (स्वस्तिक हॉस्पिटल)

- **Address:** Plot No. 3, Shamshabad Road, Kaveri Vihar Phase 1, Tajganj, Agra, Uttar Pradesh 282001
- **Phone:** +91 87914 83838 · +91 81938 38152
- **Hours:** Open 24 hours, 7 days a week

## Licence

The **code** in this repository is released under the [MIT License](LICENSE).

The hospital's name, details, doctor information, photos (loaded from Google Maps) and patient reviews belong to Swastik Hospital and their respective owners. They are not covered by the MIT License.

## Author

Built by [MOHILKUMAR](https://github.com/MOHILKUMAR).
