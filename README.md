# VendIQ — Smart Vending Operations Dashboard

An AI-powered operations dashboard for vending machine businesses. Single-page, self-contained, no backend required.

## Features

- **Fleet map** with color-coded status pins (stockout risk, anomalies, healthy)
- **Optimal route generator** — sequences machines by urgency and geography
- **AI Insights feed** with reasoning modals ("Why this recommendation?")
- **Conversational AI assistant** — ask questions about your fleet in plain English
- **90-day revenue forecast** with what-if sliders (pricing, route optimization, product mix)
- **Prospect mapping** — scored potential new locations in the metro area
- **Revenue leaderboard**, **anomaly detection**, and **product × location heatmap**
- **Before/After toggle** showing the difference between manual tracking and AI-assisted ops

## Running it

No install, no build, no dependencies to download.

**Option 1 — Double-click:**
Just open `index.html` in any modern browser.

**Option 2 — Local server (VS Code):**
Install the Live Server extension, right-click `index.html`, choose "Open with Live Server".

**Option 3 — GitHub Pages:**
Push this repo to GitHub, enable Pages in Settings → Pages → Source: main branch, root folder. Your dashboard will be live at `https://<username>.github.io/<repo-name>/`.

## Data

All data is generated synthetically in-browser on page load using a seeded random function — same numbers every time. Edit the `MACHINE_DEFS` array in the script section to customize machine names, locations, or stories.

## Tech

- HTML + CSS + vanilla JavaScript (no framework)
- [Leaflet](https://leafletjs.com/) for the map (via CDN)
- [Chart.js](https://www.chartjs.org/) for all charts (via CDN)
- [CARTO dark tiles](https://carto.com/basemaps/) for map styling

## Customization pointers

- **Change the city**: edit the `METRO_CENTER` constant and the coordinate offsets in `generateMachineCoord()`
- **Change machine names/types**: edit the `MACHINE_DEFS` array
- **Change baked-in stories**: modify the `story` property on individual machines and update corresponding insights in `generateInsights()`
- **Swap the color palette**: edit the CSS variables at the top of the `<style>` block (`--accent`, `--bg-0`, etc.)
- **Add chat patterns**: extend the regex matchers in `generateResponse()`

## License

MIT. Use it, fork it, ship it.
