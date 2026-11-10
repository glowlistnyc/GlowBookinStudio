# Glow Booking Studio — Career Clarity Coaching (bilingual site)

Static HTML/CSS site. No build step, no framework, no tracking.
Works on GitHub Pages or Cloudflare Pages as-is.

## File structure
```
/
├── index.html                  Root: redirects to /ja/ (or /en/ for English browsers)
├── styles.css                  Shared stylesheet (language-aware fonts)
├── sitemap.xml
├── robots.txt
├── CNAME                       Custom domain for GitHub Pages (glowbookingstudio.com)
├── 404.html
├── ja/
│   ├── index.html              Japanese home (11 sections)
│   └── blog/
│       ├── index.html          Blog list (JA)
│       └── kaeru-ka-mayottara/
│           └── index.html      Sample post (JA) — rewrite before publishing
└── en/
    ├── index.html              English home (11 sections)
    └── blog/
        ├── index.html          Journal list (EN)
        └── when-youre-unsure-about-changing-jobs/
            └── index.html      Sample post (EN) — rewrite before publishing
```

## Already wired in
- Booking CTA (every primary button): `https://calendly.com/glowbookingstudio/10`
- Contact: `glowbookingstudio@gmail.com`
- JP / EN language switcher, canonical + reciprocal hreflang, sitemap, robots.

## Replace before launch (search the project for each)
- `［FIRST_NAME］` / `[FIRST_NAME]` — your first name
- `［FULL_LEGAL_NAME］` / `[FULL_LEGAL_NAME]` — if/where you use a full legal name
- `［VERIFIED_CREDENTIAL_DESCRIPTION］` / `[VERIFIED_CREDENTIAL_DESCRIPTION]` — **verified** credentials only. Do not list LCSW or any clinical/therapy license here; this is non-clinical coaching.
- `［OPTIONAL_PORTRAIT］` / `[OPTIONAL_PORTRAIT]` — swap the dashed box in About for a real photo, or delete it.
- `［PRIVACY_POLICY_URL］` / `[PRIVACY_POLICY_URL]` and `［TERMS_URL］` / `[TERMS_URL]` — link your approved policy/terms pages (leave as placeholder until approved).
- Review all service copy (especially the $100 launch offer and the pricing terms) before going live.

## Deploy
This is the same static-hosting setup you used before.
- **GitHub Pages:** push these files to the repo root, enable Pages on `main` / root. `CNAME` sets the custom domain. Point DNS at GitHub (the four A records) in Wix.
- **Cloudflare Pages:** connect the repo, framework preset = *None*, build command = *(none)*, output directory = `/`.

## Add a blog post (no build step)
1. Duplicate a sample post folder, e.g. `ja/blog/kaeru-ka-mayottara/` → `ja/blog/your-slug/`.
2. Edit the new `index.html`: title, `<meta description>`, canonical URL, date, and body.
3. In `ja/blog/index.html` (or `en/blog/index.html`), copy one `<article class="post-item">` block and update its date, title, link, and excerpt.
4. Add the new URL to `sitemap.xml`.
5. Commit and push.

## Notes
- One `<h1>` per page, semantic landmarks, visible focus states, labeled language nav.
- No contact form, no database, no third-party scripts beyond Google Fonts.
- The disclaimer ("non-clinical coaching, not psychotherapy") appears in About and the footer on every page.
