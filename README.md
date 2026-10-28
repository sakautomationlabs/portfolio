# Sakar Sharma | QA Automation Lead Portfolio

A single-page, dark-themed personal portfolio for **Sakar Sharma**, QA Automation Lead with 13+ years of experience in Python, Playwright, Appium and AI-assisted quality engineering.

Built with plain HTML, CSS and JavaScript. There are no frameworks, no build step and no dependencies to install.

**Repository:** https://github.com/sakautomationlabs/portfolio
**Live site:** https://sakautomationlabs.github.io/portfolio/

## Features

- **Navigation:** a floating pill menu on desktop (1024px and up) and a bottom bar on tablets and phones. The active section is marked with a green dot on desktop and `aria-current` for assistive technology. The pill shrinks slightly once you scroll, and long labels shorten on smaller screens ("Freelance & PoCs" becomes "Freelance" and then "PoCs").
- **Live clock:** the visitor's local date and time, fixed at the top right.
- **About Me (hero):** greeting, role headline, profile photo and a professional summary. The first paragraph shows by default, and **(...more)** expands the rest without moving the rest of the layout.
- **Tools strip:** a scrolling row of tools with coloured brand icons.
- **Mission and Vision** cards.
- **What I do:** expandable panels (Test Automation, AI-Assisted Quality, QA Leadership), closed by default, beside a purple letter-glitch canvas that resizes as panels open and close.
- **Impact:** headline results such as regression time cut from 15-20 hours to 3h 42m and about 61% fewer production defects.
- **Projects:** four cards with animated SVG covers (Sprint Release Conductor, AI-Assisted Test-Case Generation, Self-Healing Locators, MCP Connector Module).
- **Experience:** four roles with every bullet, plus the selected automation projects under the current role.
- **Skills:** eight groups of tools as chips.
- **Freelance & PoCs:** four screenshot tiles (`demo1` to `demo4`) with a diagonal "SakAutomationLabs" watermark. Each opens its live demo in a new tab. If a screenshot file is missing, the tile shows a placeholder and keeps the watermark.
- **Education, Awards & Certifications, Additional Information.**
- **Resume:** a **Download PDF** button that downloads `Sakar_Sharma_Resume.pdf` from the same folder as the page.
- **Let's Connect:** a short message and a compact **Click Me** card with icon-only links for mobile, email, LinkedIn and GitHub. LinkedIn and GitHub open in a new tab.

## Sections

| Menu item | Section id |
|---|---|
| About Me | `#home` |
| Impact | `#impact` |
| Projects | `#projects` |
| Experience | `#experience` |
| Skills | `#skills` |
| Freelance & PoCs | `#freelance` |
| Resume | `#resume` |
| Let's Connect | `#contact` |

Education, Awards and Additional Information (`#education`, `#awards`, `#additional`) are on the page but are not in the menu.

## Tech

- HTML5 with semantic sections
- CSS custom properties, Grid and Flexbox with a dark palette
- Vanilla JavaScript (menu state, accordion-linked canvas sizing, live clock, expandable summary, screenshot fallback)
- Inline SVG for icons and project cover animations
- [Montserrat](https://fonts.google.com/specimen/Montserrat) from Google Fonts, with system font fallbacks

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site: markup, CSS and JavaScript |
| `screenshots/Sak_Profile.png` | Profile photo shown in the hero (also used for link previews) |
| `screenshots/demo1.png` to `demo4.png` | Thumbnails for the Freelance & PoCs section |
| `Sakar_Sharma_Resume.pdf` | Resume served by the **Download PDF** button |
| `README.md` | This file |

Keep `index.html` and the PDF in the repository root, with the images inside a `screenshots` folder next to them.

The Freelance & PoCs tiles link to `https://sakautomationlabs.github.io/portfolio/demo/demo1` through `demo4`. Those demo pages are separate from this file and must exist at those addresses (for example `demo/demo1/index.html` in the repository), or the links will open a "404" page.

## Run locally

1. Put `index.html` and `Sakar_Sharma_Resume.pdf` in one folder, with a `screenshots` folder beside them.
2. Open `index.html` in any modern browser. An internet connection is only needed for the Google Fonts stylesheet.

## Deploy with GitHub Pages

1. Commit `index.html`, `Sakar_Sharma_Resume.pdf` and the `screenshots` folder to the repository root.
2. In the repository, open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. The site will be available at `https://sakautomationlabs.github.io/portfolio/`.

## Customize

- **Text and sections:** edit the HTML directly. Each section is a `<section>` with the ids listed above.
- **Colors and fonts:** change the variables in the `:root` block at the top of the `<style>` tag (`--bg`, `--sec` for the purple accent, `--white`, `--font`).
- **Professional summary:** the text in the hero is in `.about-text`. The first paragraph is always visible and the rest sits in `#more-text`.
- **Resume PDF:** replace `Sakar_Sharma_Resume.pdf` with your new file, keeping the same name (or update the `href` on the Download PDF button).
- **Demo screenshots and links:** replace `screenshots/demo1.png` to `demo4.png`, and edit the links in the Freelance & PoCs section. The watermark text is inside the `.demo::after` rule in the CSS.
- **Profile photo:** replace `screenshots/Sak_Profile.png`. The image tag declares 280 x 390 pixels, so keep roughly that aspect ratio.
- **Contact details:** update the `tel:`, `mailto:` and profile links in the Click Me card under Let's Connect. Icon sizes are controlled by `--t` (tile) and `--i` (icon) on `.cbox`.
- **Link previews:** the `canonical`, `og:` tags and structured data in the `<head>` use `https://sakautomationlabs.github.io/portfolio/`. Update them if the site address changes.

## Accessibility and performance

- A "Skip to content" link, visible keyboard focus styles and `aria-current` on the active menu item.
- Decorative graphics are hidden from screen readers, and project covers have text labels. Icon-only links have `aria-label` text.
- A logical heading order (`h1` to `h2` to `h3`).
- Animations stop for visitors who have *reduce motion* enabled, and the tools strip becomes a static, wrapped list.
- The page is one HTML file of about 65 KB. The profile photo declares its size and loads with high priority to avoid layout shifts, and the demo screenshots load lazily.

## Credits

- Visual design inspired by the **Dark Minimal** Astro template (MIT License).
- Brand icons from [Simple Icons](https://simpleicons.org/) (CC0). Playwright, BrowserStack and SQL use simple custom icons.
- Montserrat font by Julieta Ulanovsky and contributors, under the SIL Open Font License.

## License

© 2026 Sakar Sharma. All rights reserved by SakAutomationLabs.