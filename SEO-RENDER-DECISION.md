# SEO Render Decision

The four commercial-intent SEO pages (`toppik-alternative.html`, `hairline-powder-for-men.html`, `hair-density-filler-for-men.html`, `hairo-vs-meld.html`) are generated as plain static HTML files in this same Vercel project, served directly with `cleanUrls: true` so they resolve at extensionless paths (e.g. `/toppik-alternative`).

We chose this over adding a `/blog` renderer or a CMS/SSG build step because the site is already a zero-build static deploy and the page volume is small and stable: hand-authored static pages keep the stack dependency-free, ship instantly, and reuse the existing `policies.css` design system and footer with no new tooling.

If the page count grows into the dozens or needs frequent non-technical edits, revisit and introduce a lightweight content layer (a Markdown-to-HTML build step or a headless CMS) at that point.
