# Welcome Kit (static site)

This is a fully static, client-side web app that generates a two‑page A4 Welcome Kit PDF.

Features:
- A4 layout with header, candidate photo auto‑crop (face detection), and footer
- Upload photo with face-api.js TinyFaceDetector (models in `./models`)
- Download multi‑page PDF (html2canvas + jsPDF)
- Page 2 mirrors details entered on Page 1

## Run locally
Open `welcomkit.html` directly in a modern browser, or serve the folder via any static server.

On Windows PowerShell using Python (optional):

```powershell
python -m http.server 8080 ; # then open http://localhost:8080/
```

## Host on GitHub Pages
1) Commit and push this repo to GitHub (already done if you see it online).
2) In your GitHub repo: Settings → Pages → Build and deployment:
	- Source: Deploy from a branch
	- Branch: `main` / root (`/`)
3) Save. Your site will be published at:

```
https://<your-username>.github.io/welcome-kit/
```

This repo includes an `index.html` that redirects to `welcomkit.html`, so Pages loads correctly.

## Notes
- Keep the `models/` folder at the same level as the HTML so face-api.js can load model files via relative paths.
- Assets referenced by the HTML (images, backgrounds) must remain alongside the HTML or update the paths accordingly.
- All logic runs entirely in the browser; no backend required.