# Guide de Contribution — KairoOS (tous repos)

Merci de contribuer à KairoOS ! 🕹️ Ce fichier s'applique à tous les repos de l'orga
sauf s'ils ont leur propre `CONTRIBUTING.md`.

## Règles générales

1. **Commits conventionnels, en anglais** : `feat: ...`, `fix: ...`, `refactor: ...`, `docs: ...`
2. **Branches** : `feature/nom`, `fix/nom`. PR vers `dev` pour l'app, vers `main` pour plugins/themes/website.
3. **Gamepad-first** : tout élément interactif doit être atteignable et utilisable à la manette
   (D-Pad = déplacement, A = valider, B = retour).
4. **Le core ne connaît aucun plugin** : supprimer un plugin ne doit jamais faire crasher l'app.

## Par repo

| Repo | Checks avant PR |
|------|-----------------|
| `KairoOS` (Rust) | `cargo fmt`, `cargo clippy`, `cargo test` |
| `KairoOS` (frontend) | `npx tsc --noEmit`, `npm run build` |
| `kairos-plugins` | dossier `pseudo-nom/` avec `plugin.json` valide + `README.md` |
| `kairos-themes` | dossier `pseudo-nom/` avec JSON valide + `README.md` |

## Publier un plugin / thème (communauté)

Pas besoin de PR : ajoutez votre dossier dans `community/` en push direct,
nommé `votre-pseudo-nom` (ex : `flo-achievements`). Les noms sans préfixe
sont réservés aux plugins/thèmes officiels (PR requise, revue de l'équipe).
