# CS1 Exercise Session

Static site for cs.jodenthal.com. `index.html` links to the weekly gallery in
`slides.html`; clicking a first-slide preview opens the corresponding PDF in a new tab.

The gallery and its public assets are generated from the TA workspace:

```sh
python3 scripts/export-slides.py
```

Run this from the TA workspace root before publishing. It synchronises the latest
weekly `slides.pdf` files, first-page PNG previews and topic lists. Add topics for
new weeks in `scripts/slides-metadata.json`. The normal weekly build command
(`python3 scripts/build-week.py NN`) also runs the export.

Only public slide PDFs and preview images belong in `slides/` and `previews/`.
Instructor notes, grading feedback and solution references stay in the TA workspace.
The site needs no server-side code or JavaScript. Publish the `main` branch using
the repository's existing GitHub Pages configuration; keep `CNAME` unchanged.
