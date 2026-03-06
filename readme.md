# GDS Analytics Dashboard
**West Bengal Circle — DV List 1, January 2026**

A fully static, production-ready analytics dashboard for GDS candidate data.

---

## 📁 Project Structure

```
gds-site/
├── index.html          ← Main HTML (entry point)
├── assets/
│   └── favicon.svg     ← Browser favicon
├── css/
│   ├── main.css        ← Layout, sidebar, typography
│   ├── components.css  ← Cards, tables, pills
│   └── charts.css      ← Chart wrapper styles
└── js/
    ├── data.js         ← All data + color constants
    ├── charts.js       ← Chart.js chart definitions
    └── app.js          ← Navigation, UI, table, filters
```

---

## 🖥️ Run Locally

### Option 1 — VS Code Live Server (Recommended)
1. Open the `gds-site/` folder in VS Code
2. Install the **Live Server** extension
3. Right-click `index.html` → **Open with Live Server**
4. Opens at `http://127.0.0.1:5500`

### Option 2 — Python (no install needed)
```bash
cd gds-site
python3 -m http.server 8080
# Open http://localhost:8080
```

### Option 3 — Node.js (`serve` package)
```bash
cd gds-site
npx serve .
# Opens at http://localhost:3000
```

### Option 4 — Just open the file
Double-click `index.html` in your file manager.  
> ⚠️ Some browsers block local font requests. Use a local server for best results.

---

## 🚀 Deploy / Host

### Netlify (Easiest — free)
1. Go to https://app.netlify.com/drop
2. Drag and drop the entire `gds-site/` folder
3. Your site is live in 30 seconds with a free HTTPS URL

### Vercel (free)
```bash
npm i -g vercel
cd gds-site
vercel
```

### GitHub Pages (free)
1. Create a new GitHub repo
2. Push the contents of `gds-site/` into the repo root
3. Go to **Settings → Pages → Source → main branch**
4. Your site is live at `https://<username>.github.io/<repo>`

### Traditional web hosting (cPanel / shared hosting)
1. Zip the contents of `gds-site/`
2. Upload via **File Manager** or FTP to `public_html/`
3. Access via your domain

---

## 🛠️ Tech Stack

| Technology | Purpose | CDN? |
|------------|---------|------|
| HTML5      | Structure | — |
| CSS3 (custom) | Styling, layout, responsive | — |
| Vanilla JavaScript (ES6+) | Navigation, UI, table | — |
| [Chart.js 4](https://www.chartjs.org/) | All charts | ✅ cdnjs |
| [Google Fonts](https://fonts.google.com/) | Inter + DM Mono | ✅ |

**Zero build tools. Zero npm. Zero frameworks.**  
Just HTML + CSS + JS — works anywhere.

---

## 📊 Features

- **5 dashboard views**: Overview, Division Analysis, Post Category, Community, Performance
- **Interactive filters**: Click division chips to filter stacked charts
- **Data table**: Search + filter by post type and community
- **Responsive**: Works on mobile, tablet, and desktop
- **Dark theme**: Professional dark UI with colored accents

---

## 🔧 Customise

To update data, edit `js/data.js` — all numbers are in clearly labelled constants at the top of the file.

To change colors, edit the `COMMUNITY_COLORS`, `POST_COLORS`, and `DIV_COLORS` arrays in `js/data.js`.

To add a new chart, add a canvas in `index.html`, build the chart function in `js/charts.js`, and call it from `js/app.js`.
