# Little Shishyas Chess Academy

## Update the website

Edit **content.json** in VS Code. You do not need to change `index.html` for routine content updates.

- `academy`: name, brand lines, location and address.
- `hero`: tagline, headline, supporting text and button labels.
- `navigation`: navigation labels and the accessible navigation label.
- `whyChess`: heading, introduction and benefits.
- `courses`: heading, introduction and course names. No fees are displayed on the page.
- `classes.offline` and `classes.online`: class titles, descriptions, schedules and poster button labels.
- `classes.features`: coaching features.
- `contact`: phone numbers, contact labels and enquiry message.
- `footer`: the back-to-top label.
- `page`: browser title and search description.

Keep valid JSON syntax: use double quotes around text, commas between entries, and no trailing commas. For text containing an apostrophe, double quotes work as usual.

Example: change the offline schedule in `content.json`:

```json
"schedule": "Tuesday, Thursday and Saturday. Contact us for timings and available batches."
```

The page reads `content.json` when it loads. The document title, description, headings and visible contact details are updated from that file.

## Posters

Keep `offline-poster.jpg` and `online-poster.jpg` alongside `index.html`. To update a poster, replace its image using the same filename. The filenames are currently defined in `index.html`, so rename the files there too if you use different names. Fees appear only in the posters; editing `content.json` does not change text printed inside an image.

## Preview and publish

Run a small local web server from this folder to preview the site, because the page loads `content.json` with `fetch`:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000> in a browser. JavaScript must be enabled for content changes to appear. Opening `index.html` directly with a `file://` URL may prevent `content.json` from loading.

For the first installation, copy `index.html`, `content.json`, `offline-poster.jpg` and `online-poster.jpg` into your existing repository. Keep existing GitHub workflow and custom-domain files.

Commit and push these files to the branch configured for GitHub Pages. Once deployment succeeds, refresh the website. For later text edits, commit and push `content.json`; include poster images when you replace them.

The WhatsApp destination is currently configured in `index.html`; update the `wa.me` number there if the destination changes. All files and content delivered to visitors are public. There is no admin login or backend. These changes do not configure country restrictions.
