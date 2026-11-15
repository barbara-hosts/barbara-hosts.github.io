# Events Host Portfolio

A fast, single-page portfolio website for an events host or MC, built with plain HTML and CSS. There is no build step, framework or dependency. It is designed to be hosted free on GitHub Pages.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site: styles and script are inline |
| `404.html` | Custom "page not found" page that GitHub Pages serves automatically |
| `.nojekyll` | Tells GitHub Pages to serve files as they are, skipping Jekyll processing |
| `favicon.svg` | Small icon shown in the browser tab |
| `og-image.png` | Preview image shown when your link is shared (replace with your real name) |
| `robots.txt` | Tells search engines they may list your site |
| `sitemap.xml` | Tells search engines which pages exist |
| `LAUNCH-CHECKLIST.md` | Tick-list to complete before sharing your link |
| `GETTING-STARTED.md` | Step-by-step guide for beginners |
| `README.md` | This guide |

## Customise it

Open `index.html` in a text editor and replace the placeholder content:

1. **Name**: search for `Your Name` (in `<title>`, the hero heading and the footer) and for the `YN` logo initials.
2. **Description**: update the `<meta name="description">` tag. Search engines show this text.
3. **Recent events**: edit the `<li>` items in the `#events` section (year, event, venue and guest count).
4. **Hosting types**: edit the three blocks in `#hosting`.
5. **Reviews**: replace the placeholder quotes in `#kind-words` with real client quotes.
6. **Contact**: change `you@example.com` and the Instagram and LinkedIn links.
7. **Colours**: edit the variables at the top of the `<style>` block (`--curtain`, `--blush`, `--brass`).

Repeat the name change in `404.html`.

## Preview locally

Open `index.html` in your browser. For a closer match to the live site, run a local server from this folder:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy to GitHub Pages

1. Create a **public** repository named `barbara-hosts.github.io` under the `barbara-hosts` organization.
2. Upload all files in this folder (**Add file → Upload files**) and commit.
3. Open **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Your site goes live at `https://barbara-hosts.github.io` within a few minutes.

If you use a different repository name, the site will be at `https://barbara-hosts.github.io/repo-name/`. In that case change the link in `404.html` from `href="/"` to `href="/repo-name/"`.

### Custom domain (optional)

Under **Settings → Pages → Custom domain**, enter your domain (for example `yourname.com`). Then add the DNS records GitHub lists for you at your domain registrar. Tick **Enforce HTTPS** once it becomes available.

## Adding photos

Put images in an `images/` folder, then reference them in `index.html`, for example:

```html
<img src="images/stage.jpg" alt="Hosting the Tech Summit main stage" width="800" height="533" loading="lazy">
```

Always include descriptive `alt` text, and compress images (aim for under 300 KB each) so the page stays fast.

## Notes

- Fonts (Big Shoulders Display and DM Sans) load from Google Fonts. If they fail to load, the site falls back to system fonts.
- The page is responsive and was checked at 1280px and 390px widths with no horizontal scrolling.
- The hero spotlight follows the pointer and is purely decorative. Smooth scrolling is turned off for visitors who prefer reduced motion.
