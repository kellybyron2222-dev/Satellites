# 3D Satellite Tracking Dashboard

This project is a GitHub Pages-friendly frontend that renders a full-screen CesiumJS globe and tracks live LEO / VLEO satellites from two TLE sources:

- Celestrak: https://celestrak.org
- Ivan Stanojevic's TLE API: https://ivanstanojevic.me

The dashboard merges both feeds into a single deduplicated JavaScript Map keyed by the 5-digit NORAD ID, parses each TLE with satellite.js, and updates bright point markers in real time on the globe.

## Features

- Full-screen interactive 3D globe
- Transparent sidebar with satellite count and active satellite list
- Live TLE ingestion and deduplication
- Real-time position updates via requestAnimationFrame
- Ready for deployment on GitHub Pages

## Quick Start

1. Open the repository in a browser or serve the folder locally.
2. Launch `index.html` directly, or use a simple static server such as:

   ```bash
   python -m http.server 8000
   ```

3. Visit `http://localhost:8000/` in your browser.

## Deployment

GitHub Pages can serve this repository directly as a static site. After pushing the files to GitHub, enable Pages in the repository settings and use the root folder as the deployment source.

## Notes

- The dashboard fetches TLE data client-side from the live endpoints listed above.
- Some third-party APIs may require CORS or rate-limit allowances depending on your browser environment.
