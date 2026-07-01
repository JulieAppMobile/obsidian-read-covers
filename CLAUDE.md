# obsidian-read-covers — REPO PUBLIC IMAGES COUVERTURES

> Ce repo public sert les images de couvertures via raw GitHub URL utilisées par `mobile/constants/stories.ts`.
> Pour la VUE GLOBALE du business, lire d'abord :
> - `~/Documents/MASTER_OVERVIEW.md`
> - `~/Documents/PROJECT_MAP.md`
> - `~/Documents/ACTIVE_CONVERSATIONS.md`
>
> Dernière mise à jour : 2026-07-01

---

## 📚 Mémoire partagée — auto-import

@/Users/mrs.julief/Documents/CLAUDE_SHARED_MEMORY/MEMORY.md
@/Users/mrs.julief/Documents/CLAUDE_SHARED_MEMORY/couvertures_livres.md

---

## 📋 Process couverture

1. Julie génère l'image via **Gemini** (prompt généré par `agent-couverture-livre`)
2. Image compressée en **JPG 900px** de large
3. Push dans ce repo (nom = slug du livre)
4. Dans `obsidian-read/mobile/constants/stories.ts` : utiliser URL `https://raw.githubusercontent.com/[user]/obsidian-read-covers/main/[slug].jpg?v=N`
5. **Bumper le `?v=N`** à chaque nouvelle version pour casser le cache

---

## 🖼 Couvertures actuelles

| Slug | Roman | Version actuelle |
|---|---|---|
| `a-charge-a-coeur.jpg` | À charge, à cœur | v2 |
| `hors-antenne.jpg` | Hors antenne | v2 |
| `sous-le-masque.jpg` | Sous le masque | v2 |
| `la-cible.jpg` | La Cible | v2 (titre en haut) |
| `une-nouvelle-partition.jpg` | Une Nouvelle Partition | v3 (titre en haut) |
| `sang-et-serment.jpg` | Sang et Serment | v1 |
| `noublie-pas-mon-prenom.jpg` | N'oublie pas mon prénom | v1 |
| `pour-de-faux.jpg` | Pour de faux | v1 (titre dessiné par l'app, `coverStyle: confession`) |

> Note : les `.png` sources ne sont plus dans ce repo (seul le `.jpg` 900px est servi à l'app). Originaux sauvegardés dans `OBSIDIANREAD/OBSIDIAN_READ_FUNNEL/ROMANS_LONGS/<roman>/`.

### À ajouter quand le roman est publié
- `sloane-et-cole.jpg`
- `le-onzieme-etage.jpg`
- `lyra-chade.jpg`

---

## 🚨 Règles

1. **Titre en haut** de la couverture (pas en bas) — sinon crop dans le grid 2x2 de l'app.
2. **JPG 900px** max de large (compression pour ne pas ralentir le chargement mobile).
3. **Toujours bumper `?v=N`** dans stories.ts à chaque nouvelle version pour casser le cache.
4. **Naming** : slug du livre exactement, kebab-case, ASCII (pas d'accents).

---

*Pour les conv qui touchent à ce dossier, mettre à jour `~/Documents/ACTIVE_CONVERSATIONS.md` en fin de session.*
