# Keerthish G — Portfolio (作品集)

```
portfolio/
├── vercel.json          ← tells Vercel to serve the public/ folder
├── README.md
└── public/
    ├── index.html       ← the whole website (loads /portfolio.pdf)
    └── portfolio.pdf    ← your 27-page portfolio, bundled
```

## Deploy to Vercel
1. Push this folder to a GitHub repository (or drag it into vercel.com → Add New → Project).
2. Framework preset: **Other**. No build command. Output directory: **public** (already set in `vercel.json`).
3. Deploy. The site loads `https://your-domain.vercel.app/portfolio.pdf` automatically.

Netlify / Cloudflare Pages: set the publish directory to `public`.

## Run locally
Browsers block PDF loading when `index.html` is double-clicked, so serve the `public` folder:

```
cd public
python -m http.server 8000
```
Then open http://localhost:8000 (or use `npx serve public`, or VS Code "Live Server" opened on the public folder).

## Updating the portfolio
Replace `public/portfolio.pdf` with the new file (keep the name `portfolio.pdf`).
If chapter pages move, edit the `CHAPTERS` list near the top of the script in `index.html`.
Switches at the top of the script: `JAPANESE_PAPER_MODE`, `INK_REVEAL`.
