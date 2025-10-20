# CSUF MPA — Early Exit Survey (Program Dropouts)

Static single-page survey to collect anonymous feedback from students who left the MPA program.

- Live file: [index.html](index.html)  
- Key scripts in that file: [`validateSection`](index.html), [`saveSection`](index.html), [`submitForm`](index.html), [`downloadCSV`](index.html), [`convertToCSV`](index.html), [`showSection`](index.html)

## Purpose

This lightweight survey is intended to capture why students left the program and suggestions for improvement. Responses are submitted to Formspree and a downloadable CSV backup is provided client-side.

## Features

- Progress bar and multi-section navigation (4 sections)
- Client-side validation and per-section autosave (see [`validateSection`](index.html) and [`saveSection`](index.html))
- Submit to Formspree via [`submitForm`](index.html)
- Download a local CSV backup via [`downloadCSV`](index.html)
- Mobile-friendly, accessible form layout

## Quick Start

1. Open [index.html](index.html) in a browser (double-click or serve via a static server).
2. Complete the sections and submit. If submission fails, use the "Download CSV" button to save a local copy.

## Deployment (GitHub Pages)

1. Commit `index.html` and this `README.md` to your repo.
2. Enable GitHub Pages from repository settings and point it to the repository root (or `gh-pages` branch).
3. Access the survey at: `https://<YOUR-GITHUB-USERNAME>.github.io/<REPO-NAME>/index.html`

## Data collection

- Submissions use Formspree endpoint defined in [index.html](index.html).
- Local CSV backup created by [`convertToCSV`](index.html) and downloaded by [`downloadCSV`](index.html).
- Program staff may export saved responses from Formspree for analysis.

## Customization

- Edit questions, labels, or validation directly in [index.html](index.html).
- To change submission endpoint, update the `action` on the `<form>` element in [index.html](index.html) and adjust [`submitForm`](index.html) if needed.

## Privacy & Use

- Recommended to inform respondents that responses are collected for program improvement and may be reviewed by program leadership.
- Anonymous responses are supported by skipping name/email fields.

## Troubleshooting

- Ensure JavaScript is enabled in the browser.
- If submission fails:
  - Use the "Download CSV" button to save responses and email to program staff (<dpadams@fullerton.edu>).
  - Check browser console for errors originating from functions such as [`submitForm`](index.html).

## Contact

David P. Adams, Ph.D — <dpadams@fullerton.edu>

---

Last updated: October 2025
