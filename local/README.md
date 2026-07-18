# Local offline mirror (rasterbator)

Snapshot of https://posterizer.online/rasterbator/ as deployed 2026-07-18,
modified to run fully offline:

- all asset URLs rewritten from posterizer.online to relative paths
- jQuery vendored locally (was CDN)
- sample image replaced: upstream points at lorempixel.com, which is dead
  (broken on the live site too); now bundles static/images/sample.jpg
- Google Analytics snippet removed
- Roboto fonts vendored under static/font/roboto/

Everything runs client-side (jsPDF + JSZip in the browser); no backend needed.

Run: `python3 -m http.server 8000` in this directory, open http://localhost:8000
