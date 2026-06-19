# Licences tierces — BRASS Cue

BRASS Cue redistribue des composants tiers. Ce fichier satisfait les obligations
d'attribution et de licence (notamment GPLv3 pour FFmpeg).

## FFmpeg (GPL-3.0-or-later) — composant le plus important

Ce produit utilise **FFmpeg** (https://ffmpeg.org), un projet tiers, **sous licence
GNU GPL version 3**. *FFmpeg is a trademark of Fabrice Bellard, originator of the
FFmpeg project.*

- **Binaires redistribués** : `ffmpeg` et `ffprobe`, fournis via les paquets npm
  `ffmpeg-static` (5.3.0) et `ffprobe-static`.
- **Version FFmpeg** : **7.0.2** (fournie sous le tag de release `b6.1.1` de
  eugeneware/ffmpeg-static@5.3.0 ; le « b6.1.1 » est le nom du tag npm, pas la version
  du binaire — vérifiable via `ffmpeg -version` ou le `ffmpeg.README` livré).
- **Builds** : gyan.dev (Windows), John Van Sickle (Linux), evermeet.cx / osxexperts.net (macOS), compilés avec `--enable-gpl --enable-version3`.
- **Texte de licence complet** : voir `ffmpeg.LICENSE` (GPLv3) livré dans
  `resources/app.asar.unpacked/node_modules/ffmpeg-static/` de cette application.
- **Flags de configuration du build** : voir `ffmpeg.README` au même emplacement.

### Offre de code source correspondante (GPLv3 §6)

Le code source correspondant à la version de FFmpeg redistribuée est disponible :

- Source officielle FFmpeg 7.0.2 : https://ffmpeg.org/releases/ffmpeg-7.0.2.tar.xz
- Release des binaires utilisés : https://github.com/eugeneware/ffmpeg-static/releases/tag/b6.1.1
- Builds Windows : https://www.gyan.dev/ffmpeg/builds/
- Builds Linux : https://www.johnvansickle.com/ffmpeg/

Sur demande écrite à **ACS Partners**, et pendant au moins trois (3) ans, une copie du
code source correspondant peut être fournie.

> Note : FFmpeg est invoqué par BRASS Cue en tant que **processus séparé** (ligne de
> commande). Le code propre de BRASS Cue n'est pas un travail dérivé de FFmpeg.

## Autres dépendances

Le reste des dépendances embarquées est sous licences permissives (MIT, ISC, Apache-2.0,
BSD-2/3-Clause, BlueOak-1.0.0, 0BSD…). Aucune autre dépendance n'impose d'obligation
copyleft. Voir l'analyse complète : `docs/LICENSE-ANALYSIS.md`.

- React, React-DOM — MIT
- @dnd-kit/* , dnd-kit-sortable-tree — MIT
- yauzl, yazl — MIT
- uuid — MIT
- ffprobe-static (wrapper npm) — MIT (le binaire ffprobe reste GPLv3, voir ci-dessus)
