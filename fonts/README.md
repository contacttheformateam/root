# /fonts/ — self-hosted webfonts

These fonts are served from this domain so that no visitor IP address is
transmitted to Google (or any other third party) when a page loads.

## Files expected in this directory

| File | Family | Weight | Used by |
|---|---|---|---|
| `archivo-500.woff2` | Archivo | 500 | headings, subtitles |
| `archivo-700.woff2` | Archivo | 700 | h1, h2 |
| `karla-400.woff2` | Karla | 400 | body text |
| `karla-500.woff2` | Karla | 500 | body emphasis |
| `karla-700.woff2` | Karla | 700 | `<strong>` in privacy policy (optional) |
| `jetbrains-mono-400.woff2` | JetBrains Mono | 400 | eyebrow, plate, dates, footer |
| `jetbrains-mono-500.woff2` | JetBrains Mono | 500 | mono emphasis |

## Licences

All three families are licensed under the SIL Open Font License 1.1,
which explicitly permits self-hosting and redistribution.

- Archivo — Omnibus-Type — https://github.com/Omnibus-Type/Archivo
- Karla — Jonny Pinhorn — https://github.com/googlefonts/karla
- JetBrains Mono — JetBrains — https://github.com/JetBrains/JetBrainsMono

Keep a copy of each family's `OFL.txt` in this directory. The OFL requires
the licence text to accompany redistributed font files.

## Regenerating

Latin subset, woff2 only, via google-webfonts-helper (https://gwfh.mranftl.com):

    curl -L -o archivo.zip "https://gwfh.mranftl.com/api/fonts/archivo?download=zip&subsets=latin&formats=woff2&variants=500,700"
    curl -L -o karla.zip "https://gwfh.mranftl.com/api/fonts/karla?download=zip&subsets=latin&formats=woff2&variants=regular,500,700"
    curl -L -o jetbrains.zip "https://gwfh.mranftl.com/api/fonts/jetbrains-mono?download=zip&subsets=latin&formats=woff2&variants=regular,500"

Downloaded filenames include a version string (e.g. `archivo-v19-latin-500.woff2`).
Rename them to the plain names in the table above so the CSS keeps working
across future font updates.
