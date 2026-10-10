# AI2ASE 2027 Hugo source

Website: https://ai-2-ase.github.io/

The `hugo-source` branch stores the editable workshop source. The `master` branch in `ai-2-ase/ai-2-ase.github.io` stores the generated static website used by GitHub Pages. Source changes do not publish automatically.

## Build

Use Hugo **0.95.0 extended**, the version installed on the original maintainer's machine and verified to reproduce the published 2026 homepage, call for papers, dates, schedule, and papers pages byte for byte. The legacy Netlify configuration retains its original 0.87.0 setting. Keep `go.mod` and `go.sum` pinned to the existing Wowchemy revision.

From this source directory:

```sh
hugo
hugo server --disableFastRender --i18n-warnings
```

`hugo` generates the static site in `public/`. Review the result before copying it into a separate checkout of the `master` branch and committing/pushing. Preserve historical files in that checkout; do not use a copy command with deletion enabled. Never merge `master` into `hugo-source` or vice versa.

## Content

- `content/home/title.md`: workshop title.
- `content/home/theme.md`: introduction, date, venue, theme.
- `content/home/speakers.md`: speakers section.
- `content/authors/`: people and portraits.
- `content/home/organizing_comittee.md`: organizer section.
- `content/cop/_index.md`: call for papers.
- `content/dates/_index.md`: deadlines.
- `content/schedule/_index.md`: program.
- `content/papers/_index.md`: accepted papers.
- `config/_default/menus.yaml`: navigation and earlier editions.
- `assets/scss/custom.scss`: homepage text width, title typography, and section headings. Section padding is set in the home widgets. Earlier editions use the template's built-in nested menu.
- `config/_default/config.yaml`: base URL and Hugo configuration.

The 2027 edition lists Diana Cai, Felix Draxler, Samuel Kaski, and Sungsoo Ahn as invited speakers. The call for papers retains the 2026 topics, paper lengths, submission format, and non-archival policy. Paper submission is November 15, 2026 (11:59 PM PST); notification is November 30, 2026. Theme, venue, workshop date, camera-ready deadline, submission-site URL, schedule, and accepted papers remain to be announced. Portrait provenance is recorded in `SPEAKER-SOURCES.md`. The 2026 organizing committee is retained pending updates. Prior speakers remain as draft source profiles and are excluded from the new speaker list. All older editions remain linked.
