# Glow Booking Studio — Career Clarity Coaching (bilingual site)

Static HTML/CSS, no build step, no framework, no tracking.
Goal of the site: get visitors to book the free 10-minute intro call.

## File structure (deployable)
```
/
├── index.html                 Root: sends visitors to /ja/ (or /en/ for English browsers)
├── 404.html
├── robots.txt
├── sitemap.xml
├── assets/
│   ├── styles.css             Shared stylesheet (language-aware fonts)
│   ├── img/
│   │   └── portrait.jpg       Coach portrait (provided photo, web-optimized)
│   └── illust/                Illustration PLACEHOLDERS — replace with real Linustock art
│       ├── hero-lineart.svg
│       ├── career-dilemma.svg
│       └── session-steps.svg
├── ja/
│   └── index.html             Japanese page
└── en/
    └── index.html             English page
```
Kept OUTSIDE this folder, not deployed:
- `../glow-coaching-blog-drafts/` — blog drafts (JA/EN). Not public until real articles are ready.

## Already set
- CTA (every primary button): `https://calendly.com/glowbookingstudio/10`
- Contact: `glowbookingstudio@gmail.com` · Footer location: New York, NY
- Coach: Haruna Otani (大谷はるな) · credential shown as "LMSW, New York" (background), service clearly stated as **non-clinical coaching**.
- JP / EN switcher, canonical + reciprocal hreflang, sitemap, robots.

## Illustrations
`assets/illust/` contains three simple, warm, original line illustrations (hero sunrise/path, a gentle fork for "who this is for," two cups for the session). They're free to use and already placed on the page. Keep them, or swap in your own / Linustock art (https://www.linustock.com/vectors) by saving over the same filenames. The hero art is hidden on mobile by design; change `.hero-illust { display:none }` in the stylesheet if you want it shown on phones.

## Not shown until you provide the real content
- **Privacy Policy / Service Terms** links are commented out in the footer of both pages (no broken placeholder links go live). When you have real URLs, uncomment those lines and insert the URLs.
- The About name/credential text is live (you confirmed it). To change wording, edit `ja/index.html` and `en/index.html` directly.

## Credentials note (important)
This site presents you as a **non-clinical career coach**, with LMSW shown as professional background. It does not market therapy, counseling, diagnosis, or treatment. In New York an LMSW cannot provide independent clinical/psychotherapy services outside a supervised/approved setting, so avoid "therapist"/"counselor"/"psychotherapy" wording for this service. If you ever want to adjust how the license is described, confirm title usage with the NY State Board for Social Work (SWBD@nysed.gov). (Not legal advice.)

## Deploy — pick ONE host (do not mix the two)
Confirm your current hosting before changing anything.
- **GitHub Pages:** push these files to the repo root; enable Pages on `main` / root. For the custom domain, add a `CNAME` file containing `glowbookingstudio.com` AND point DNS to GitHub's four A records. (No `CNAME` file is included here on purpose — add it only if you choose GitHub Pages.)
- **Cloudflare Pages:** connect the repo; framework preset = None; build command = none; output dir = `/`. Set the custom domain in the Cloudflare dashboard. Do **not** add a GitHub `CNAME` file.

Do not change DNS until you've confirmed which host is live.

## Blog (later)
Drafts live in `../glow-coaching-blog-drafts/`. When an article is ready, move its folder into `ja/blog/<slug>/` (or `en/blog/<slug>/`), add a link where you want it (kept out of the main nav by request), and add the URL to `sitemap.xml`.
