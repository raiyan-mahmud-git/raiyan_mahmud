# Raiyan Mahmud: Portfolio

My personal portfolio: machine-learning, NLP and data projects built in Python, plus a few web projects. It is a single static page with no build step and no framework.

**Live site:** https://raiyan-mahmud-git.github.io/portfolio/

## What is on the page

- **Projects.** Six selected projects chosen to show different skills, each with a diagram of how it works and links to the code. The chess engine, Flo, the SMS spam classifier and the Sea Level Predictor also have live demos.
- **About, skills and languages.**
- **Education and courses.**
- **Certifications.** Each certificate opens in an accessible dialog with a link to verify it.
- **Contact form.** Messages are delivered to my email through [FormSubmit](https://formsubmit.co/).

## Design and engineering notes

- **One file.** `index.html` holds the markup, styles and script. There is nothing to install or build.
- **Works without JavaScript.** Navigation and the contact form still work. JavaScript only adds the mobile menu, the theme toggle, the certificate dialog and the hero animation.
- **Light and dark themes.** It follows the system setting, and the toggle stores a choice only when it differs from the system.
- **Accessibility.** Semantic HTML, a skip link, visible keyboard focus, a native `<dialog>` that returns focus to the button that opened it, and `aria-current` on the section you are viewing. Motion is switched off under `prefers-reduced-motion`.
- **Modern CSS.** `light-dark()` colour tokens, scroll-driven animations (as progressive enhancement), and `backdrop-filter` for the glass panels, with a fallback where it is not supported.
- **Diagrams.** The hero scatter plot and the project diagrams are inline SVG. The hero plot uses made-up data and the other diagrams are labelled schematics, not real results.
- **Fonts.** Newsreader and Hanken Grotesk from Google Fonts, with system fonts as a fallback.

## Run it locally

Opening `index.html` directly works for most things, but the contact form needs the page to be served over `http`. From this folder:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Images

Put these files in an `images/` folder next to `index.html`. The page hides any image that is missing.

| File | Used for |
| --- | --- |
| `profile.jpg` | Portrait in the About section |
| `flo-screenshot.jpg` | Screenshot of Flo |
| `cert-ml-freecodecamp.jpg` | Machine Learning with Python certificate |
| `cert-data-freecodecamp.jpg` | Data Analysis with Python certificate |
| `cert-ai-ibm.jpg` | IBM AI Fundamentals certificate |
| `cert-ai-fluency-anthropic.jpg` | Anthropic AI Fluency certificate |
| `cert-sql-sololearn.jpg` | SoloLearn SQL Intermediate certificate |

## Deploy to GitHub Pages

1. Push `index.html` and the `images/` folder to the `main` branch.
2. In the repository, open **Settings → Pages**.
3. Set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save.

## Contact form setup

The form posts to FormSubmit using the same address as its `action`:

```html
<form action="https://formsubmit.co/raiyanmahmud484@gmail.com" method="POST">
```

- The first submission sends an activation email to that address. Messages are not delivered until you click the link in it. Check spam too.
- With JavaScript on, the form sends in the background and shows a success or error message. If no reply can be read, it says it could not confirm delivery and offers a pre-filled email link as a fallback.
- To send messages somewhere else, change the address in the form's `action`.

## Contact

raiyanmahmud484@gmail.com
