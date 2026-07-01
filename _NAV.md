# 🧭 obsidian-read-covers — Fil d'Ariane

> 🖼️ **IMAGES** : repo public des couvertures de livres, servies à l'app/site.

⬆️ **Parent** : [`../OBSIDIAN_READ_HUB.md`](../OBSIDIAN_READ_HUB.md)
📍 **Source de vérité** : 1 couverture = 1 fichier `[slug].jpg` (kebab-case, ASCII, titre en haut, 900px max).

## ⬇️ Ce qu'il y a dedans
- `*.jpg` — couvertures compressées 900px servies à l'app (et `.png` sources parfois).
- `CLAUDE.md` — process couverture (génération Gemini → compression → push → bump `?v=N`).
- `README.md` — doc process.

## 🔗 Liens croisés
- Consommées par l'app via URL raw GitHub dans le catalogue ([`../obsidian-read/mobile/`](../obsidian-read/_NAV.md))
- Prompts de génération archivés dans [`../OBSIDIANREAD/COVERS_REFERENCES/`](../OBSIDIANREAD/_NAV.md)

## ⚠️ Notes / dette (audit 2026-06-26)
- 🔴 Servies via `raw.githubusercontent.com` = **pas un CDN**, rate-limité (429 possible en charge).
  → court terme : jsDelivr (`cdn.jsdelivr.net/gh/USER/REPO@main/…`) · long terme : Supabase Storage.
- Le cache-busting `?v=N` est le pattern faible → préférer noms fingerprintés + `Cache-Control: immutable`.
