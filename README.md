# مردّد القرآن

Arabic-first Quran memorization player: pick a reciter and ayah range, listen with repeats, study on a Madinah mushaf page, and review with tafsir — all in a single static page.

## Features

- **Playback** — Choose reciter, surah, ayah range, per-ayah repeats, and full-range repeats
- **Mushaf view** — Madinah mushaf (QCF V2) with the current ayah highlighted while listening
- **Memorization aids**
  - Hide / reveal the practice range (`H`, or the toolbar button)
  - Click an ayah to hide or show it alone
  - Hover a hidden word for a temporary peek
  - `←` reveals the next hidden word in reading order
- **Tafsir** — Side accordion of التفسير الميسّر; identical explanations are grouped with shared ayah numbers
- **Navigation** — Page number plus previous / next (right = previous, left = next)
- **Session restore** — Selections, hide state, last position, and theme persist across refresh
- **Dark mode** — Toggle in the header
- **In-app guide** — دليل الاستخدام explains the workflow

## Run locally

No build step. Open the page in a browser:

```bash
# optional: simple local server
npx serve .
# or
python -m http.server 8080
```

Then open `index.html` (or the URL the server prints).

> Audio and mushaf fonts load from the network, so an internet connection is required.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `H` | Hide or show the whole practice range |
| `←` | Reveal the next hidden word |
| `Esc` | Close the tutorial modal |

## Data sources

| Source | Used for |
| --- | --- |
| [EveryAyah](https://everyayah.com/) | Recitation audio |
| [Al Quran Cloud](https://alquran.cloud/) | Text & التفسير الميسّر |
| [Quran.com API](https://api.quran.com/) / Quran Foundation fonts | QCF V2 mushaf words & page fonts |

## Project layout

```
index.html      # app (UI, styles, logic)
.impeccable.md  # design context
```

## License

Use and adapt freely for personal learning and non-commercial sharing. Respect the terms of the upstream audio, text, and font providers.
