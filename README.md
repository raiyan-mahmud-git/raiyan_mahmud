# Raiyan Mahmud: Portfolio

Personal portfolio featuring machine-learning, NLP, data and web projects built in Python and JavaScript. The site is a static page with no build step or framework.

**Live site:** https://raiyan-mahmud-git.github.io/raiyan_mahmud/

## What is on the page

- **Seven projects:** Chess Lab, DocuMind, Flo, TinyDL, Book Price Scraper, Cats & Dogs Image Classifier, and RPS Arena. Each project links to its live demo or showcase and source code.
- **Project screenshots** show the apps in use and open in an accessible image-preview dialog. The dialog closes with its Close button, by clicking outside, or with Escape.
- **About, skills and languages.**
- **Education and courses.**
- **Certifications.** Each certificate can open in an accessible dialog and includes a verification link.
- **Contact form.** Messages are delivered to my email through [FormSubmit](https://formsubmit.co/).

Cats & Dogs extends a freeCodeCamp challenge. TinyDL was inspired by Andrej Karpathy's micrograd.

## Design and engineering notes

- **One page.** `index.html` holds the markup, styles and script. There is nothing to install or build. The `images/` folder contains project screenshots and optional portrait and certificate images.
- **Works without JavaScript.** Page navigation and the contact form still use regular links and form submission. JavaScript adds the mobile menu, theme toggle, image-preview dialogs, and enhanced contact-form feedback.
- **Light and dark themes.** The page follows the system setting. The toggle stores a choice only when it differs from the system preference.
- **Accessibility.** Semantic HTML, a skip link, visible keyboard focus, keyboard-operable image previews, a native `<dialog>` that returns focus to its opener, and `aria-current` on the section in view. Motion respects `prefers-reduced-motion`.
- **Fonts.** Hanken Grotesk from Google Fonts, with system fonts as a fallback.

## Images

Place these files in an `images/` folder next to `index.html`. Missing optional portrait and certificate images are hidden gracefully.

| File | Used for |
| --- | --- |
| `chess-lab.png` | Chess Lab project screenshot |
| `documind-preview.png` | DocuMind showcase screenshot |
| `flo-screenshot.png` | Flo dashboard screenshot |
| `tinydl-preview.png` | TinyDL digit-demo screenshot |
| `book-tracker.png` | Book Price Scraper screenshot |
| `cats-dogs.png` | Cats & Dogs classifier screenshot |
| `rps-arena.png` | RPS Arena screenshot |
| `profile.jpg` | Portrait in the About section (optional) |
| `cert-ml-freecodecamp.jpg` | Machine Learning with Python certificate (optional) |
| `cert-data-freecodecamp.jpg` | Data Analysis with Python certificate (optional) |
| `cert-ai-ibm.jpg` | IBM AI Fundamentals certificate (optional) |
| `cert-mcp-anthropic.jpg` | Anthropic Introduction to Model Context Protocol certificate (optional) |
| `cert-sql-sololearn.jpg` | SoloLearn SQL Intermediate certificate (optional) |

## Run it locally

Opening `index.html` directly works for most features. The contact form needs the page served over HTTP. From this folder, run:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy to GitHub Pages

1. Push `index.html`, `README.md`, and the `images/` folder to the `main` branch.
2. In the repository, open **Settings → Pages**.
3. Set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save.

## Contact form setup

The form posts to FormSubmit using the same address as its `action`:

```html
<form action="https://formsubmit.co/raiyanmahmud484@gmail.com" method="POST">
```

- The first submission sends an activation email to that address. Messages are not delivered until you click the link in it. Check spam too.
- With JavaScript enabled, the form sends in the background and shows feedback. If it cannot confirm delivery, it offers a pre-filled email link as a fallback.
- To send messages somewhere else, change the address in the form's `action`.

## Contact

raiyanmahmud484@gmail.com
