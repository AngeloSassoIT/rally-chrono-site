# Rally Chrono — Website

Static website for [Rally Chrono](https://apps.apple.com/), the regularity rally stopwatch for co-drivers.

Hosted on GitHub Pages, served at https://rallychrono.app.

## Structure

| File | Purpose |
|---|---|
| `index.html` | Homepage with hero, features and download CTA |
| `privacy.html` | Privacy policy (required by App Store) |
| `support.html` | Support page with FAQ (required by App Store) |
| `terms.html` | Terms of use |
| `404.html` | Custom not-found page (served by GitHub Pages on missing URLs) |
| `style.css` | Shared dark-theme stylesheet |
| `CNAME` | Custom domain for GitHub Pages (`rallychrono.app`) |
| `robots.txt` | Crawler instructions |
| `sitemap.xml` | Sitemap for search engines |

## Local preview

```bash
cd Files
python3 -m http.server 8000
```

Then open http://localhost:8000

## Deploy

1. Push to the `main` branch of the GitHub repo.
2. Repo Settings → Pages → Source: `main` / `/ (root)`.
3. Set custom domain to `rallychrono.app` and tick **Enforce HTTPS**.

## DNS configuration (custom domain)

At your registrar (Cloudflare, Porkbun, etc.) for `rallychrono.app`:

| Type | Name | Value |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `<your-github-username>.github.io` |

Wait 5-15 minutes for DNS propagation, then enable HTTPS in repo settings.

## License

© 2026 Angelo Sasso. All rights reserved.
