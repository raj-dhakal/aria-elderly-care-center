# aria-elderly-care-center

Official website project for Aria Elderly Care Center, built with HTML5, CSS3, and Bootstrap 5.

## Folder structure

```
aria-elderly-care-center/
├── index.html                 Home page
├── README.md
│
├── assets/
│   ├── css/
│   │   ├── base/
│   │   │   ├── variables.css  Brand colors, fonts, sizes (edit these first)
│   │   │   └── global.css     Page-wide defaults, headings, section titles
│   │   ├── components/
│   │   │   ├── buttons.css    Green / outline / pill buttons
│   │   │   └── cards.css      Icon circles, service cards, quote cards
│   │   ├── layout/
│   │   │   ├── header.css     Top navbar (every page)
│   │   │   └── footer.css     Footer (every page)
│   │   └── pages/
│   │       └── home.css       Sections that only appear on index.html
│   │
│   ├── images/                Photos and logo used on the website
│   └── js/
│       └── main.js            Custom scripts (empty for now)
│
└── docs/                      Planning files (layouts, diagrams) – not part of the site
```

## How the CSS works

Every page links the CSS files in this order, from general to specific.
Later files can override earlier ones.

1. `base/` – variables and global defaults
2. `components/` – reusable pieces
3. `layout/` – header and footer
4. `pages/<page>.css` – that page's own sections

To add a new page (for example `about.html`):

1. Copy the `<head>`, `<header>` and `<footer>` from `index.html`.
2. Create `assets/css/pages/about.css`.
3. Swap the last `<link>` to point at `pages/about.css`.

## Conventions

- File and image names: lowercase, words joined with hyphens, no spaces
  (`personal-care.jpg`, not `Personal Care.JPG`).
- Colors: always use a variable from `variables.css` (`var(--green-dark)`),
  never a raw hex code inside other files.
- Class names describe *what* something is (`.service-card`, `.hero-text`),
  not how it looks (`.green-box`).
