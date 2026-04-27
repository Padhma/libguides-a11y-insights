# 🔍 Research Guides Pa11y

**Comprehensive WCAG 2.1 AA compliance scanning for LibGuides.**

Research Guides Pa11y is a browser bookmarklet that helps LibGuide owners create accessible and inclusive guides for all users, including those who rely on screen readers and other assistive technologies. Built for the University of Michigan Library, this tool is designed to work on any LibGuides CMS instance (version 2 and later).

---

## Why This Tool?

Most accessibility testing tools are designed for general websites. When used on LibGuides, they flag issues in the platform's header, footer, navigation, and system code, things that guide owners can't control. The results are often technical and difficult to act on without a web development background.

Research Guides Pa11y solves this by:

- **Scoping scans to guide content only**, skipping platform, chrome, and admin elements
- **Providing fix instructions written for the LibGuides editor**
- **Adding custom checks for common LibGuides patterns** that generic tools miss

---

## Features

- **Accessibility Score** — An at-a-glance rating out of 100 for each page
- **Dual-Layer Scanning** — Industry-standard [axe-core](https://github.com/dequelabs/axe-core) engine plus custom LibGuides-specific checks
- **Plain-Language Explanations** — Every issue is described without jargon
- **LibGuides-Specific Fix Instructions** — Step-by-step guidance tailored to the LibGuides CMS editor
- **Visual Highlighting** — Click "Show on Page" to highlight and scroll to the problematic element
- **Single Page & Multi-Page Scanning** — Scan the current page or every page in the guide
- **Issue Categorization** — Issues are classified as violations, warnings, or best practices
- **Privacy-First** — All processing happens locally in your browser; no data is transmitted to external servers
- **Free & Open Source** — No costs, subscriptions, or usage limits

### What It Checks

| Category | Examples |
|---|---|
| Images | Missing alt attributes, generic/filename alt text, alt text quality |
| Headings | Empty headings, skipped heading levels, image-only headings |
| Links | URL-only link text, generic phrases ("click here"), links opening in new windows without warning, visually indistinguishable links |
| Color Contrast | Text failing WCAG 2.1 AA contrast ratios (4.5:1 normal, 3:1 large) |
| Tables | Missing headers, invalid scope attributes, layout tables, missing semantic structure |
| Forms | Input fields without labels, buttons without labels |
| Embedded Content | Iframes missing titles, duplicate iframe names |
| Structure | Duplicate IDs (common from copy-pasting), empty containers, icon-only elements without labels |

---

## Installation

### 1. Show your bookmarks bar

- **Windows/Linux:** `Ctrl + Shift + B`
- **Mac:** `Cmd + Shift + B`

### 2. Install the bookmarklet

Visit the [Research Guides Pa11y documentation site](https://padhma.github.io/research-guides-pa11y/) and **drag** the gold button labeled **"🔍 Research Guides Pa11y V2.0.0"** to your bookmarks bar.

> **Note:** Drag the button — don't click it. Clicking it on the documentation site won't do anything useful.

---

## Usage

1. **Navigate to any live LibGuides page** (the public-facing version or a preview mode of an unpublished guide)
2. **Click the bookmarklet** in your bookmarks bar
3. **Review the results** in the sidebar that appears on the right side of the page
4. **Fix issues** using the plain-language instructions provided for each one

### Tips

- Use **"Show on Page"** to highlight and scroll to the problematic element
- Use **"Show All Pages"** to scan every page in the guide at once
- **Re-run the scan** after making fixes to see your updated score
- The sidebar **auto-closes after 15 minutes** of inactivity
- Use the **drag handle** on the left edge of the sidebar to resize it
- Use the **collapse arrow** to minimize the sidebar without closing it

---

## How the Score Works

The accessibility score starts at 100 and takes deductions based on what the tool finds:

| Priority | Deduction per instance | Max deduction |
|---|---|---|
| Violation (WCAG failure) | 10 points | 30 points |
| Warning (usability issue) | 5 points | 20 points |
| Best Practice | 2 points | 10 points |

The minimum score is 15. The score is meant as a quick indicator, not a precise audit grade.

---

## Limitations

- **Catches ~60% of WCAG issues.** Complex issues like meaningful image descriptions, logical reading order, and content structure still require human review.
- **Automated testing is sometimes wrong.** For example, displaying full URLs in citation examples is intentional — the tool may still flag it. Use your judgment.
- **Some flagged patterns require viewing the HTML source** to understand or fix.
- **Does not replace manual accessibility testing.** Keyboard navigation, screen reader testing, and human evaluation are still essential.
- **Only works on live LibGuides pages or preview pages.** Not designed for the LibGuides admin editor view or non-LibGuides websites.

---

## Technology

- **[axe-core](https://github.com/dequelabs/axe-core) v4.7.2** — The same accessibility engine trusted by Google, Microsoft, and accessibility professionals worldwide
- **Custom LibGuides checks** — Specialized rules for patterns that generic tools miss
- **Vanilla JavaScript** — No frameworks, no build step, no dependencies beyond axe-core (loaded from CDN at runtime)

---

## Browser Support

| Browser | Supported |
|---|---|
| Chrome | ✅ |
| Firefox | ✅ |
| Safari | ✅ |
| Edge | ✅ |
| Internet Explorer | ❌ |

---

## Other Accessibility Testing Tools

Research Guides Pa11y is one tool in your toolkit. These complement it well:

- **[WAVE Browser Extension](https://wave.webaim.org/extension/)** — General-purpose accessibility evaluation (Chrome, Firefox, Edge)
---

## Feedback

We'd love to hear from you:
- [Contact the developer](mailto:padhma@umich.edu)
- **GitHub Issues:** [Open an issue](https://github.com/padhma/libguides-a11y-insights/issues) on this repository
---

# License
 
This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).
 
You are free to use, share, and adapt this tool for non-commercial purposes, with appropriate credit. Commercial use is not permitted without prior written permission.
 
Built for the University of Michigan Library.
