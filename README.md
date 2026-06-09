# wallet-tracker-docs

Documentation website for the **Wallet Balance Tracker** Google Sheets™ add-on.

Live at: `https://wallet-tracker-docs.vercel.app`

## Pages

| Page | URL |
|------|-----|
| Home | `/` |
| Privacy Policy | `/privacy.html` |
| Terms of Service | `/terms.html` |
| Support | `/support.html` |

## Local Development

```bash
# Install dependencies
npm install

# Start dev server (opens at http://localhost:5173)
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview
```

## Deploy to Vercel

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → New Project
3. Import your GitHub repo
4. Build settings (auto-detected):
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
5. Click **Deploy**

Done. Vercel will give you a URL like `https://wallet-tracker-docs.vercel.app`.

## Store Listing URLs

Use these in your Google Workspace Marketplace listing:

```
Privacy Policy : https://wallet-tracker-docs.vercel.app/privacy.html
Terms of Service: https://wallet-tracker-docs.vercel.app/terms.html
Support         : https://wallet-tracker-docs.vercel.app/support.html
```

## Stack

- [Vite](https://vitejs.dev/) — build tool
- Vanilla HTML + CSS — no framework needed for a static docs site
- [Vercel](https://vercel.com/) — hosting
