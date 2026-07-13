# Lookalikes — The Gallery

A simple, single-page gallery of celebrity lookalikes. Built with plain HTML, CSS, and JavaScript — no frameworks, no build step.

🔗 **Live site:** https://manjiriparab.github.io/lookalike-gallery/

## What it does

- Displays groups of people who resemble each other, with photos, names, and short bios shown on equal footing (no "primary vs match" hierarchy).
- Includes a search bar to filter groups by any name in the group.
- All content is pulled from `data.json`, so entries can be added or edited without touching any code.

## Files

| File | Purpose |
|---|---|
| `index.html` | The page itself — layout, styling, and the script that loads and renders entries |
| `data.json` | All lookalike entries. Edit this file to update the gallery |

## How to add or edit entries

Open `data.json` and add a new object to the `groups` array. Each group is a list of people who look alike:

```json
{
  "people": [
    { "name": "Full Name", "bio": "One short line about them", "photo": "https://example.com/photo.jpg" }
  ]
}
```

- `photo` can be left as `""` to show a colored initials placeholder instead of an image.
- A group can have as many people as you want (e.g. one real person + multiple celebrity matches).
- Only use photos you have the rights to use — e.g. your own images, or reusable-licensed photos from sources like Wikimedia Commons.

Commit and push the updated `data.json`, and GitHub Pages will pick up the change automatically — usually within a minute or two.

## Hosting

This site runs on **GitHub Pages** (free, for public repos). It's served from the `Master` branch via **Settings → Pages** in the repo.

## Local preview

Because the page loads `data.json` via `fetch()`, opening `index.html` directly by double-clicking it won't load the data (browsers block local file fetches). To preview locally, run a simple local server from the project folder, for example:

```bash
python3 -m http.server
```

Then open `http://localhost:8000` in your browser.

## Notes

Lookalike pairings shown here are subjective and fan-sourced, not verified claims about the individuals featured.
