# Sakar Sharma | QA Automation Lead Portfolio

A single-page, dark-themed personal portfolio for **Sakar Sharma**, QA Automation Lead with 13+ years of experience in Python, Playwright, Appium and AI-assisted quality engineering.

Built with plain HTML, CSS and JavaScript. There are no frameworks, no build step and no dependencies to install.

**Repository:** https://github.com/sakautomationlabs/sak_portfolio

## Features

- **Navigation:** a floating pill menu on desktop (1024px and up) and a bottom bar on tablets and phones, with a green dot on the active section.
- **Live clock:** the visitor's local date and time, fixed at the top right.
- **Hero:** greeting, role headline and a scrolling strip of tools with colored brand icons.
- **Mission and Vision** cards.
- **What I do:** expandable panels (Test Automation, AI-Assisted Quality, QA Leadership) beside a purple letter-glitch canvas that resizes as panels open and close.
- **Impact:** headline results such as regression time cut from 15-20 hours to 3h 42m and about 61% fewer production defects.
- **Projects:** four cards with animated SVG covers (Sprint Release Conductor, AI-Assisted Test-Case Generation, Self-Healing Locators, MCP Connector Module).
- **Experience, Skills, Education, Awards & Certifications, Additional Information.**
- **Resume:** a **Download PDF** button that serves the resume embedded in the page.
- **Let's Connect:** mobile, email, LinkedIn and GitHub links. LinkedIn and GitHub open in a new tab.

## Sections

| Menu item | Section id |
|---|---|
| About Me | `#home` |
| Impact | `#impact` |
| Projects | `#projects` |
| Experience | `#experience` |
| Skills | `#skills` |
| Resume | `#resume` |
| Let's Connect | `#contact` |

Education, Awards and Additional Information (`#education`, `#awards`, `#additional`) are on the page but are not in the menu.

## Tech

- HTML5 with semantic sections
- CSS custom properties, Grid and Flexbox with a dark palette
- Vanilla JavaScript (nav state, accordion-linked canvas sizing, live clock, resume download)
- Inline SVG for icons and project cover animations
- [Montserrat](https://fonts.google.com/specimen/Montserrat) from Google Fonts, with system font fallbacks

## Run locally

1. Download `portfolio.html`.
2. Open it in any modern browser. An internet connection is only needed for the Google Fonts stylesheet.

## Deploy with GitHub Pages

1. Rename `portfolio.html` to `index.html` and commit it to the repository root.
2. In the repository, open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. The site will be available at `https://sakautomationlabs.github.io/sak_portfolio/`.

## Customize

- **Text and sections:** edit the HTML directly. Each section is a `<section>` with the ids listed above.
- **Colors and fonts:** change the variables in the `:root` block at the top of the `<style>` tag (`--bg`, `--sec` for the purple accent, `--white`, `--font`).
- **Resume PDF:** the PDF is stored as a Base64 string in the `B64` variable in the last `<script>` block. To update it, convert your new PDF to Base64 and replace that string:

  ```bash
  base64 -w 0 Sakar_Sharma_Resume.pdf
  ```

- **Contact details:** update the `tel:`, `mailto:` and profile links in the Let's Connect section.

## Accessibility and performance

- Decorative graphics are hidden from screen readers, and project covers have text labels.
- Visible keyboard focus styles.
- Animations stop for visitors who have *reduce motion* enabled.
- The whole site is one HTML file of about 230 KB, most of it the embedded resume.

## Credits

- Visual design inspired by the **Dark Minimal** Astro template (MIT License).
- Brand icons from [Simple Icons](https://simpleicons.org/) (CC0). Playwright, BrowserStack and SQL use simple custom icons.
- Montserrat font by Julieta Ulanovsky and contributors, under the SIL Open Font License.

## License

© 2026 Sakar Sharma. All rights reserved by SakAutomationLabs.
