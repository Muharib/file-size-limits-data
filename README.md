# File size limits & social media image sizes — open data

Two small, hand-checked datasets, free to reuse:

| File | What it holds |
|---|---|
| [`data/file-size-limits.json`](data/file-size-limits.json) · [`.csv`](data/file-size-limits.csv) | Maximum file size (and duration, pages, accepted formats) of **34 places people send files to**: WhatsApp, Telegram, Signal, Messenger, iMessage, Gmail, Outlook, Yahoo, Proton, Instagram, X, LinkedIn, YouTube, TikTok, Discord, Google Drive, WeTransfer, and French online administrations (CAF, France Travail, impots.gouv, ANTS, Démarches simplifiées…) |
| [`data/social-media-image-sizes.json`](data/social-media-image-sizes.json) · [`.csv`](data/social-media-image-sizes.csv) | Recommended **upload** sizes (px) of 21 image formats on Instagram, Facebook, X, LinkedIn, YouTube, TikTok and Pinterest |

## How the data is made

- Every value cites its **source** (the platform's own help page whenever one exists) and the day it was **last checked**.
- `confidence: "low"` marks a value that could not be confirmed on an official page (third-party guides, forum answers). Treat it as "to verify".
- Units are kept as the platform states them: `MB` = decimal (16 MB = 16,000,000 bytes), `MiB` = binary (20 MiB = 20,971,520 bytes). When a platform does not say, the decimal reading is used — it is the stricter one. `bytes` gives the exact figure.
- A destination has one or more `rules`, checked in order: the first rule whose `kinds` (video, image, audio, pdf, other) matches the file applies. `overMax` says how a larger file can still go through (e.g. WhatsApp: as a document, up to 2 GB). `countsEncoded: true` = the limit counts the e-mail's Base64 size (≈ +37 %), not the size on disk.
- Social sizes are the size to **upload**, not the (smaller) size the network displays.

## Browse it

The same data, with explanations, a checker that tests your own file, and translations (English, French, Spanish):

- File size limits: https://awesometoolkit.com/en/file-size-limits
- File requirements of French online procedures: https://awesometoolkit.com/fr/online-procedures-file-requirements
- Social media image sizes: https://awesometoolkit.com/en/social-media-image-sizes

## Corrections

Platforms change their limits. If a value is wrong or out of date, open an issue or a pull request with a link to the source.

## Licence

[CC BY 4.0](LICENSE) — reuse it anywhere, commercial use included, with credit:

> Data: [Awesome Toolkit](https://awesometoolkit.com) — file size limits & social media image sizes (CC BY 4.0)
