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
npm install
npm run dev       # http://localhost:5173
npm run build     # production build → dist/
npm run preview   # preview the build locally
```

## Deploy to Vercel

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → New Project → import repo
3. Build settings (auto-detected):
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
4. Click **Deploy**

## Store Listing URLs

```
Privacy Policy : https://wallet-tracker-docs.vercel.app/privacy.html
Terms of Service: https://wallet-tracker-docs.vercel.app/terms.html
Support         : https://wallet-tracker-docs.vercel.app/support.html
```

## Releasing a New Version

### 1. Deploy a new version from the library project

```
Extensions → Apps Script (in your library project)
→ Deploy → Manage deployments
→ ✏️ Edit the existing deployment
→ Version dropdown → "New version"
→ Add a description (e.g. "v2 - batch mode fix")
→ Deploy
```

The Script ID never changes. Only the version number increments.

### 2. How users get the update

| How they installed | What they need to do |
|---|---|
| **Option A — copied the Sheet** | Go to Extensions → Apps Script → Libraries → WalletTracker → change Version dropdown to the new number → Save |
| **Option B — added library manually** | Same as above, or select HEAD to always auto-update |
| **HEAD (development mode)** | Nothing — they get every deploy instantly |

> ⚠️ Users who copied the Sheet have a **frozen version** from the day they copied it. They won't update automatically. There is no push-notification mechanism in Apps Script. You must communicate new versions via release notes, GitHub, or a version-check toast in the script itself.

### 3. Recommended release discipline

```
1. Test your changes against a local test Sheet (not the public copy)
2. Deploy → New version (do NOT push untested code to HEAD if users rely on it)
3. Update this README + CHANGELOG with what changed
4. Update the docs site if setup steps changed
5. Optionally: update the public "Make a Copy" Sheet to link the new version
   (new copiers will then get the latest version baked in)
```

### 4. Updating the public "Make a Copy" Sheet

This is the step most people miss. After deploying a new library version:

```
1. Open the source Sheet (the one linked in the hero button)
2. Extensions → Apps Script → Libraries → WalletTracker
3. Change Version to the new number → Save
4. The Script ID link in the docs still works — new copiers now get the updated version
```

Existing copies are unaffected. Only new copies pick up the version you set here.

## Stack

- [Vite](https://vitejs.dev/) — build tool
- Vanilla HTML + CSS
- [@vercel/analytics](https://vercel.com/docs/analytics) — page view tracking
- [Vercel](https://vercel.com/) — hosting

## Built by

- [buildbyravi](https://github.com/buildbyravi)
- [CryptoExplor](https://github.com/CryptoExplor)
