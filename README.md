# Academic website of Iulian-Teodor Voicilă

Personal academic page: research, publications, teaching and CV.

Live at: https://iulian-voicila.github.io/

The site is plain HTML, CSS and a small JavaScript file. There is no build step and nothing to install; GitHub Pages serves the files as they are.

## Files

| File | Content |
| --- | --- |
| `index.html` | Overview (home page) |
| `research.html` | Research themes, projects, software and open data, patents |
| `project-*.html` | One page per project |
| `publications.html` | Full publication list with search and filters |
| `teaching.html`, `about.html`, `contact.html` | Teaching, biography and certificates, contact |
| `cv.html` | Printable CV, linked from the footer ("Academic CV") |
| `assets/` | Portrait, favicon, CV in PDF |
| `publications.bib` | BibTeX for all publications |
| `data/publications.json` | The publication list in JSON |
| `styles.css`, `app.js` | Layout and the publication filter / mobile menu |
| `.nojekyll` | Tells GitHub Pages to serve the files without Jekyll |

## Preview locally

Open `index.html` in a browser, or run a small local server from this folder:

```
python -m http.server 8000
```

and go to http://localhost:8000.

## Add a publication

1. In `publications.html`, copy an existing `<article class="pub-row" ...>` block of the same type and paste it at the right place (the list is ordered by year, newest first).
2. Change the `id`, the text (title, authors, venue) and the DOI link.
3. Update the attributes used by the filters:
   - `data-year`: the year;
   - `data-type`: one of the types already used (Journal article, Conference paper, Book, Patent application, Dataset, Software);
   - `data-topic`: one or more topics separated by `|`, written exactly as in the Topic filter;
   - `data-search`: title, authors and venue, so the search box finds the record.
4. If the year is new, add it to the Year filter (`<select name="year">`) and to the bar chart above the list.
5. Add the record to `publications.bib` and to `data/publications.json`.
6. If it should appear on the home page, copy the same block into the "Selected publications" section of `index.html`.
7. Update the numbers on the home page (outputs catalogued, Google Scholar citations and h-index, and the date in the note under them) and the "Last updated" date in the footer.

## Change the photo or the CV

- Photo: replace `assets/portrait.jpg` with a new file of the same name (a square or 4:5 portrait, at least 800 px wide). If the proportions change, adjust the `width` and `height` of the image in `index.html`.
- CV: edit `cv.html`, open it in a browser, use **Print → Save as PDF** (no headers and footers) and save it over `assets/CV_Iulian-Teodor_Voicila.pdf`.

## Publish changes

Upload the changed files to the `main` branch of the repository (on github.com: **Add file → Upload files**, or with git). GitHub Pages republishes the site within a few minutes.

## Credits

The layout follows the academic websites of colleagues in the Department of Measurements, Electrical Apparatus and Static Converters (UNSTPB).
