# Ketan Patil · Portfolio

A cinematic, scroll-driven personal portfolio for **Ketan Patil**, Computer Science Engineer and Business Development Executive at Artonest Technosys, Surat.

**Where technology meets business.**

## What's inside

| File | What it is |
| --- | --- |
| `index.html` | The main portfolio (premium navy & brass design): animated silk hero, "How can I help you?" switcher, road-trip journey, expertise, selected work, process, credentials, contact with phone and WhatsApp. |
| `versions/cinematic.html` | The previous cinematic design, kept as a backup at `/cinematic` (not indexed). |
| `versions/gallery-tour.html` | An alternate 3D gallery tour with a walking avatar guide (uses three.js from a CDN). |
| `assets/photos/` | Ketan's photos (headshot, About portrait, graduation). |
| `assets/ketan-cutout.webp` | Background-removed portrait used in the closing scene. |
| `assets/seo/` | Social share image, headshot for Google, favicons and app icons. |
| `robots.txt`, `sitemap.xml`, `site.webmanifest` | Search engine and browser files. |
| `profile.html`, `llms.txt`, `llms-full.txt` | Text-first profile for search engines and AI assistants. |
| `vercel.json` | Clean URLs, caching for images, and `/tour` for the 3D gallery tour. |

Everything is a single self-contained HTML file. The main page needs no build step and no JavaScript libraries; only Google Fonts load from the web.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publish with GitHub Pages

1. Go to **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Pick the `main` branch and the `/ (root)` folder, then **Save**.
4. After a minute the site is live at `https://ketanpatilfreelance-star.github.io/Ketan-Patil-Portfolio/`.

## SEO

The site is set up for search and social sharing:

- Title, description and canonical URL for `https://ketan-patil-portfolio.vercel.app`.
- Open Graph and Twitter tags with a 1200×630 share image (`assets/seo/og-image.jpg`).
- Structured data (JSON-LD) describing Ketan as a Person: job title, employer, university, location, languages, skills, services and profile links.
- `robots.txt` and `sitemap.xml`. The alternate tour is marked `noindex` so it doesn't compete with the main page.
- Photos load as separate cached files, and the hero photo is preloaded.

If the site moves to another address (for example a custom domain), replace `https://ketan-patil-portfolio.vercel.app` in `index.html`, `robots.txt`, `sitemap.xml` and `versions/gallery-tour.html`.

### Get it on Google

1. Open [Google Search Console](https://search.google.com/search-console) and add a **URL prefix** property for the site address.
2. Verify with the **HTML tag** method: paste the `<meta name="google-site-verification" ...>` tag into the `<head>` of `index.html`, push, and click Verify.
3. Under **Sitemaps**, submit `sitemap.xml`.
4. Use **URL Inspection** on the home page and click **Request indexing**.

Also add the site link to LinkedIn (Contact info → Website), GitHub profile, Upwork and Instagram bio. Those links help Google find and trust the site.

## AI search (ChatGPT, Claude, Perplexity, Gemini)

AI assistants answer questions about people by searching the web and reading plain page text. Many of their crawlers don't run JavaScript, so the site also ships text-first versions:

- `profile.html` (served at `/profile`): the full profile as plain HTML, with Person, ProfilePage, FAQPage and BreadcrumbList structured data.
- `llms.txt` and `llms-full.txt`: a short index and the full profile in Markdown, following the llms.txt convention.
- `robots.txt` explicitly allows search engines and AI crawlers (GPTBot, OAI-SearchBot, ClaudeBot, Claude-SearchBot, PerplexityBot, Google-Extended and others).

To update the profile text, edit `profile.html`, `llms.txt` and `llms-full.txt` together so they stay consistent.

Also submit the site to [Bing Webmaster Tools](https://www.bing.com/webmasters) (ChatGPT search uses Bing's index; you can import from Google Search Console in one click).

## Editing details

Open `index.html` and search for `EDIT YOUR DETAILS HERE`. The `PROFILE` object holds your email and links (LinkedIn, GitHub, Upwork, résumé). Skills, journey milestones, projects and career details are plain arrays just below it.

Still to add: the names and Credly links of the 11 AWS badges, and Fiverr, Freelancer, Contra and Credly profile links.

## Contact

- Email: 96ketan@gmail.com
- LinkedIn: https://www.linkedin.com/in/ketan-patil-7205802b7/
- Upwork: https://www.upwork.com/freelancers/~011480449dd273474b
