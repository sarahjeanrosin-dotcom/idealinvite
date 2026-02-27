# 💌 Wedding Address Formatter

An AI-powered tool for formatting wedding invitation addresses consistently based on a vibe you describe. Built as a single-page web app — no backend, no install, just open and use.

**[→ Live Demo](https://YOUR-USERNAME.github.io/wedding-address-formatter)**

![screenshot placeholder](https://via.placeholder.com/800x400?text=Wedding+Address+Formatter)

---

## What it does

1. **Describe your vibe** — type something like *"formal and traditional, spell everything out, use Mr. and Mrs."* or *"modern and minimal, first names only"*
2. **Upload your guest spreadsheet** — CSV or Excel, with columns for name, street, city, state, and ZIP
3. **Get formatted addresses** — the AI applies your style consistently to every row, handling messy data and making smart assumptions along the way
4. **Download or copy** — export as CSV for mail merge or copy individual addresses

---

## Setup & Deployment

### Option 1: Run locally (no setup needed)
Just open `index.html` in any browser. Enter your Anthropic API key when prompted.

### Option 2: Deploy to GitHub Pages (free)

1. **Fork or clone this repo**
   ```bash
   git clone https://github.com/YOUR-USERNAME/wedding-address-formatter.git
   ```

2. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repo on GitHub
   - Click **Settings** → **Pages**
   - Under *Source*, select **Deploy from a branch**
   - Choose `main` branch, `/ (root)` folder
   - Click **Save**
   - Your site will be live at `https://YOUR-USERNAME.github.io/wedding-address-formatter` in ~1 minute

---

## API Key

This app uses the [Anthropic API](https://anthropic.com) to power the AI formatting. Users enter their own API key directly in the app — **the key is never stored, sent anywhere, or saved between sessions**.

To get an API key:
1. Sign up at [console.anthropic.com](https://console.anthropic.com)
2. Go to **Account → API Keys**
3. Create a new key and paste it into the app

> ⚠️ **If you're hosting this for others to use with your own key:** Be aware that API usage costs money and there are no built-in usage limits in this app. Consider adding rate limiting or restricting access if you share it publicly.

---

## Spreadsheet format

Your CSV or Excel file should have columns for:
- Guest name(s)
- Street address
- City
- State
- ZIP code

Column names don't need to be exact — the app will try to auto-detect them, and you can manually map any column. The AI is also forgiving of messy data: missing fields, combined columns, typos, and inconsistencies are handled gracefully.

**Sample format:**
| Name | Street | City | State | ZIP |
|------|--------|------|-------|-----|
| John and Jane Smith | 123 Main St | Boston | MA | 02101 |
| Dr. Robert Chen | 456 Oak Avenue | Chicago | IL | 60601 |

---

## Tech

- Vanilla HTML/CSS/JS — zero dependencies to install
- [Anthropic Claude API](https://docs.anthropic.com) for AI formatting
- [PapaParse](https://www.papaparse.com/) for CSV parsing
- [SheetJS](https://sheetjs.com/) for Excel parsing
- Hosted via GitHub Pages (static, free)

---

## License

MIT — free to use, modify, and share. If you build something cool with it, I'd love to see it.
