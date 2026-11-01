# QA report

Tested on 2 Nov 2026 with Chromium (Playwright) against a local static server.

## Automated checks run

| Check | Result |
|---|---|
| 4 pages at 390, 768, 1024 and 1440 px: horizontal overflow | No overflow on any page at any width (wide tables scroll inside their own box) |
| Images load | All images load on all pages |
| Console errors and failed requests (4xx/5xx) | None |
| Internal links and anchors (all pages) | All resolve. The only unresolved path is the portrait file named inside an HTML comment |
| Mobile menu | Opens, closes after a link is tapped, scrolls to the right section |
| Resume download | Returns the PDF (200, application/pdf) |
| Em dashes and emoji | None in the site |
| Spelling (codespell) | No errors. Spelling standardized to US English |

## Content audit

| Question | Answer |
|---|---|
| Does the homepage work for both product and business analysis applications? | Yes. The hero and "How I work" section show skills that both kinds of role look for, without splitting the site into separate tracks |
| Free of design-portfolio positioning? | Yes. Design internships are described through requirements, research and process work, and there is no link to the UI/UX portfolio |
| Evidence-based? | Yes. Figures come from the READMEs, decision log, test docs and results annexure |
| Contributions accurate? | Each case study separates "My work" and "Team work". Items needing confirmation are listed in MISSING_INFO.md |
| Product and requirements content | One combined "How I work" section; each case study shows product decisions followed by requirements and rules on the same page |
| Follows the Dribbble reference? | Lime gradient hero fading to white, serif italic and sans headline pairing, central portrait, lime project collage, tilted three-step cards, project grid, experience list with photo, lime closing CTA and oversized serif name in the footer. Testimonials from the reference were left out because there are no real ones |

## Not tested

- **External links.** GitHub links were checked against the repository list. The live demos (Vercel, Render) and LinkedIn could not be opened from the build environment.
- **Safari and Firefox.** Only Chromium was used.
- **Real devices.** Mobile was checked at a 390 px viewport, not on a phone.

## Known gaps

- The resume PDF is an interim version until Prachi provides her own.
- `og:image` uses a relative path until the site has a domain.
