# Floyd UK Website

Static site for Floyd UK (Pink Floyd tribute). Shows are loaded from `shows.json` so they can be updated without touching the HTML.

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `floyd-uk-site`).
2. Upload / push the contents of this folder (`index.html`, `shows.json`, and the image files).
3. In the repo Settings → Pages, set Source to “Deploy from a branch” and choose `main` / root.
4. The site will be live at `https://<username>.github.io/floyd-uk-site/` (or custom domain).

## How the booking bot updates shows

The Floyd UK Booking Agent can:
- Research confirmed dates
- Edit `shows.json` (add/remove objects)
- Commit and push the change

Example `shows.json` entry:
```json
{
  "venue": "Venue Name, City",
  "date": "Saturday 15 March 2026",
  "ticketUrl": "https://tickets.example.com/..."
}
```

`ticketUrl` is optional. Leave it out or set to empty string if tickets are not yet on sale.

## Netlify alternative

Connect the same GitHub repo to Netlify for the same auto-deploy behaviour (often faster and with custom domain support).

## Local testing

Open `index.html` in a browser (or use a local server: `python3 -m http.server`) so the fetch for `shows.json` works.
