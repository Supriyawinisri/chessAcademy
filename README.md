# Little Shishyas Chess Academy

## Update the website

Edit **content.json** in VS Code. You do not need to change `index.html` for routine content updates.

- `academy`: name, brand lines, location and address.
- `hero`: tagline, headline, supporting text and button labels.
- `navigation`: navigation labels and the accessible navigation label.
- `whyChess`: heading, introduction, benefit titles and descriptions, and the Courses link label.
- `faq`: homepage FAQ heading, introduction and expandable question/answer entries.
- `courses`: heading, introduction, course names and matching level descriptions, displayed on the separate `courses.html` page. No course fees are displayed.
- `classes.offline` and `classes.online`: class titles, descriptions, schedules and Courses-page button labels. `classes.online.batches` holds each batch's sessions and amount.
- `classes.features`: coaching features.
- `contact`: phone numbers, WhatsApp destination and message, directions button label, and contact labels.
- `footer`: the back-to-top label.
- `page`: browser title and search description.

Keep valid JSON syntax: use double quotes around text, commas between entries, and no trailing commas. For text containing an apostrophe, double quotes work as usual.

Example: change the offline schedule in `content.json`:

```json
"schedule": "Tuesday, Thursday and Saturday. Contact us for timings and available batches."
```

The pages read `content.json` when they load. The document title, description, headings and visible contact details are updated from that file. The homepage Courses link and Explore courses button open `courses.html`, where visitors can continue to the Online or Offline details page.

## Posters

Keep `offline-poster.jpg` and `online-poster.jpg` alongside the HTML pages. Course schedules and amounts appear on `courses.html`; `online.html` and `offline.html` focus on format details and posters. The Offline page also links to directions using the address in `content.json`. To update a poster, replace its image using the same filename. The filenames are defined in each class page, so update the matching page if you use a different name. Editing `content.json` does not change text printed inside an image.

## Preview and publish

Run a small local web server from this folder to preview the site, because the page loads `content.json` with `fetch`:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000> in a browser. JavaScript must be enabled for content changes to appear. Opening `index.html` directly with a `file://` URL may prevent `content.json` from loading.

For the first installation, copy `index.html`, `courses.html`, `offline.html`, `online.html`, `content.json`, `offline-poster.jpg` and `online-poster.jpg` into your existing repository. Keep existing GitHub workflow and custom-domain files.

Commit and push these files to the branch configured for GitHub Pages. Once deployment succeeds, refresh the website. For later text edits, commit and push `content.json`; include poster images when you replace them.

Set `contact.whatsappNumber` to the country code and phone number using digits only, with no `+`, spaces or punctuation (for example, `919566252618`). The homepage and both class pages use this value for their WhatsApp enquiry links. All files and content delivered to visitors are public. There is no admin login or backend. These changes do not configure country restrictions.
