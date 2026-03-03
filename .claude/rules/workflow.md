## Workflow

1. **Generate** — Produce a single `index.html` using Tailwind CSS via CDN. All content inline; no external files unless explicitly requested.

2. **Capture** — Take a full-page screenshot with Puppeteer (`npx puppeteer screenshot index.html --fullpage`). For pages with distinct sections, also capture individual section screenshots.

3. **Analyse** — Compare the screenshot against the reference image. Catalogue every discrepancy across:
   - Spacing and padding (measured in px)
   - Font size, weight, and line-height
   - Colour values (exact hex codes)
   - Alignment and positional accuracy
   - Border radii, shadows, and graphical treatments
   - Responsive behaviour across viewports
   - Image and icon sizing and placement

4. **Correct** — Fix every identified discrepancy in the HTML and Tailwind code.

5. **Iterate** — Re-capture and re-analyse. Repeat until within 2–3px tolerance of the reference across all visible elements.

> Minimum two complete comparison rounds are mandatory. Stop only on explicit user directive or when no discernible differences remain.
