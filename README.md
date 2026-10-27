# CS1 Exercise Session

Static site for cs.jodenthal.com. `index.html` links to the weekly gallery in
`slides.html`; clicking a first-slide preview opens the corresponding PDF in a new tab.

The gallery and its public assets are generated from the TA workspace:

```sh
python3 scripts/sync-slides.py
```

Run this from the TA workspace root before publishing. It synchronises the latest
weekly `slides.pdf` files, first-page PNG previews and topic lists. Add topics for
new weeks in `scripts/slides-metadata.json`. The normal weekly build command
(`python3 scripts/build-week.py NN`) also runs the sync.

Only public slide PDFs and preview images belong in `slides/` and `previews/`.
Instructor notes, grading feedback and solution references stay in the TA workspace.
The site needs no server-side code or JavaScript. Publish the `main` branch using
the repository's existing GitHub Pages configuration; keep `CNAME` unchanged.

PDFs are read directly from the weekly folders. There is no intermediate export folder. Shared slide design lives in the TA workspace under `shared/presentation/`; `--all --watch` rebuilds prepared decks and updates this site after successful changes.
