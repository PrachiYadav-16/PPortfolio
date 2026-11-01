# pportfolio

Portfolio of **Prachi Yadav** for product and business analysis roles. The content shows skills (discovery, requirements, prioritization, process mapping) rather than splitting the site into separate role tracks, so one site works for both kinds of application.

Plain HTML, CSS and JavaScript. No framework, no build step and no dependencies. Fonts are self-hosted.

## Structure

```
index.html                     Home: hero, approach, how I work, projects, experience, skills, about, contact
case-studies/
  fraudnet-synth.html          Case study: problem, users, decisions, requirements, rules, results
  ai-interviewer.html
  mentorconnect.html
  vayu-aqi.html
assets/
  css/style.css                All styles. Colors and fonts are set as variables at the top
  js/main.js                   Navigation, mobile menu, scroll reveal
  fonts/                       Instrument Serif and Outfit (woff2)
  img/                         Screenshots (webp) and og.png for link previews
  resume/                      Resume PDF linked from every Resume button
favicon.svg
MISSING_INFO.md                What still needs Prachi's input
QA_REPORT.md                   What was tested and the results
```

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Any static file server works. Opening `index.html` directly also works.

## Deploy

**Vercel (recommended):** create the GitHub repository `pportfolio`, push or upload these files, then in Vercel choose *Add New Project*, import `pportfolio` and click Deploy. There are no build settings to change.

**GitHub Pages:** in the repository go to *Settings > Pages*, choose *Deploy from a branch*, select `main` and `/ (root)`.

Live at https://prachi-yadav-work.vercel.app. If the domain changes, update `canonical`, `og:url` and `og:image` in each page's `<head>`.

## Updating content

Everything is plain text in the HTML files. Search for these to find what needs updating:

| What | Where |
|---|---|
| Photos | `assets/img/prachi-portrait.webp` (hero) and `assets/img/prachi-work.webp` (Experience). Transparent background, replace with the same names |
| Resume | Replace `assets/resume/Prachi_Yadav_Resume.pdf`, keeping the same file name. Every resume button on the site links to it |
| Colors and fonts | top of `assets/css/style.css` |

Convert new screenshots to webp to keep pages fast, for example `cwebp -q 80 in.png -o out.webp`.

## Content rules this site follows

- Every claim comes from Prachi's resume, her portfolio case studies, or the project repositories.
- Personal work and team work are separated on each case study.
- Model results that come from simulated data are labelled as simulated.
- Requirement tables are labelled as retrospective analysis, not original documents.
