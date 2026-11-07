# conjugation-catalog

The language packs of [Conjugation Trainer](https://github.com/ikovacs85/conjugation): the app reads
`manifest.json` from this repository's `main` branch and downloads the packs it lists, which are this
repository's release assets.

- `manifest.json`: one entry per pack (DATA_MODEL.md §1.3 in the app's repository): language, version,
  the pack schema it needs (`minAppVersion`), the download URL and size, the SHA-256 of the download and
  of the pack, and how many verbs and tenses it has.
- Releases: one per pack version, tagged `packs-<lang>-<version>`, holding `pack-<lang>-<version>.sqlite.gz`.

Packs are built and published by `tools/pack-builder` in the app's repository (its README, "Publishing
packs"); don't edit `manifest.json` by hand.

## Licence

The packs are built from Wiktionary (via Wiktextract and kaikki.org) and FrequencyWords (OpenSubtitles),
and are distributed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). The French
pack also uses Lexique 3 (CC BY-SA 4.0) for frequencies.
