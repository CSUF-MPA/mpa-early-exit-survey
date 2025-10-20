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
- **Full WCAG 2.1 AA accessibility compliance** (see [Accessibility Features](#accessibility-features))

## Accessibility Features

This survey is designed to be fully accessible to users with disabilities and follows WCAG 2.1 AA guidelines:

### Screen Reader Support

- **Semantic HTML**: Proper use of `<header>`, `<main>`, `<section>`, `<fieldset>`, and `<legend>` elements
- **ARIA labels**: Comprehensive labeling with `aria-describedby`, `aria-labelledby`, and `role` attributes
- **Live regions**: Dynamic announcements for form progress, validation errors, and section changes via `aria-live`
- **Screen reader descriptions**: Hidden descriptive text for complex form elements

### Keyboard Navigation

- **Full keyboard accessibility**: All interactive elements are keyboard accessible
- **Skip links**: Allow users to jump directly to main content
- **Arrow key navigation**: Radio button groups support arrow key navigation
- **Focus management**: Proper focus handling during section transitions
- **Tab order**: Logical tab sequence throughout the form

### Visual Accessibility

- **High contrast support**: Enhanced styles for users with `prefers-contrast: high`
- **Focus indicators**: Clear, visible focus outlines on all interactive elements
- **Reduced motion support**: Respects `prefers-reduced-motion` user preferences
- **Color independence**: Information is not conveyed through color alone

### Form Accessibility

- **Progress indicators**: Accessible progress bar with proper ARIA attributes
- **Error handling**: Clear error messages announced to screen readers
- **Field validation**: Real-time validation with accessible error reporting
- **Required field indication**: Clear marking of required fields with both visual and screen reader cues

## Quick Start

1. Open [index.html](index.html) in a browser (double-click or serve via a static server).
2. Complete the sections and submit. If submission fails, use the "Download CSV" button to save a local copy.
3. **Accessibility**: The form is fully navigable via keyboard and compatible with all major screen readers.

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
- **Accessibility note**: When modifying the form, ensure new elements include proper ARIA labels and maintain keyboard accessibility.

## Privacy & Use

- Recommended to inform respondents that responses are collected for program improvement and may be reviewed by program leadership.
- Anonymous responses are supported by skipping name/email fields.

## Troubleshooting

- Ensure JavaScript is enabled in the browser.
- **Accessibility**: The form works with JavaScript disabled for basic functionality, but enhanced accessibility features require JavaScript.
- If submission fails:
  - Use the "Download CSV" button to save responses and email to program staff (<dpadams@fullerton.edu>).
  - Check browser console for errors originating from functions such as [`submitForm`](index.html).

## Accessibility Testing

The form has been designed to work with:

- **Screen readers**: NVDA, JAWS, VoiceOver, TalkBack
- **Keyboard navigation**: Full form completion without mouse
- **Browser zoom**: Up to 200% zoom without horizontal scrolling
- **High contrast modes**: Windows High Contrast, browser extensions
- **Reduced motion**: Respects user motion preferences

For accessibility issues or suggestions, contact David P. Adams at <dpadams@fullerton.edu>.

## Contact

David P. Adams, Ph.D — <dpadams@fullerton.edu>

---

Last updated: December 2024
