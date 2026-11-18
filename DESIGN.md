# DESIGN — Réseau électrique (gameday-reseau-electrique)

Journal design (Claude). Versions datées, jamais écrasées. Livrables dans `G-DESIGN/`.

## V1 — 2026-11-18 · 3 directions sur la page Jeu

**Compris du produit** : un post Reddit quotidien où l'on garde la rue d'un village éclairée de 18:00 à minuit. La production baisse au coucher du soleil pendant que la demande monte vers 21 h : il faut stocker le surplus du début de soirée et le libérer au bon moment. Même soirée (seed) pour tous, puis une carte de fin avec score, série et invitation à commenter.

**Références** : catégorie `narratif-jeu` de `REFERENCES-DESIGN.md` V2 (lues en capture, à la demande de Gaia) + les 2 refs du brief (Cron, Baseten). Détail dans `G-DESIGN/REFS.md`.

**Pages** : `G-DESIGN/PAGES.md` (4 pages, à valider) + 7 questions produit ouvertes (contrôle, sources, prévision, échec, score, communauté, rejouer).

**Les 3 directions** (`G-DESIGN/planches/v1/`), même données de démo, même état « 20:30, on libère le stock » :

| # | Direction | Palette | Typo | Motif |
|---|-----------|---------|------|-------|
| 01 | **Veillée** | crépuscule `#1B2233`, accent lampe `#FFC46B`, réseau `#38BDF8` en donnée seulement | linéale système grasse + mono pour les chiffres | la courbe de charge en héros, 12 lampadaires au pied de la courbe |
| 02 | **Carnet** | papier `#F2EEE3`, encre `#18171C`, accent lampe `#FF9A1F` | grotesque noire capitales au trait tremblé, chiffres gras | relevé tenu à la main : le manque s'encre en noir, la pointe annoncée par une flèche griffonnée |
| 03 | **Maquette** | table `#ECEBE6`, encre `#111214`, accent énergie `#1F63FF` | linéale très condensée + mono | village-jouet isométrique sur un socle, batterie dont le niveau monte sur sa face |

**Recommandation : 02 Carnet.** Elle se reconnaît dans le feed au premier coup d'œil (la plupart des 30 jeux du concours seront sombres), le trait d'encre rend la pointe et le manque lisibles en 5 secondes, et tout se fait en SVG/CSS sans image ni 3D. La 01 est la plus sûre et la plus fidèle au brief ; la 03 est la plus « jouet » mais la plus chère à produire et la moins lisible en petit.

**Changelog V1** : création de `PAGES.md`, `REFS.md`, `planches/v1/01-veillee.html`, `02-carnet.html`, `03-maquette.html`. Chaque planche : cadre desktop 1440 × 900 + cadre mobile 390 × 844 côte à côte, 5 états du jeu en vignettes (prêt, surplus, pointe, stock à sec, déjà joué). Fichiers autonomes, s'ouvrent en double-clic.

**Attendu de Gaia** : Garder / Changer (deltas numérotés) / Essayer, + choix d'une direction et réponses aux questions de `PAGES.md`. Ensuite : `STYLE.md` puis les planches Post, Carte de fin, Séries & classement.

## V1 · validation — 2026-11-18

**Gaia retient la direction 03 « Maquette »** (et non la recommandation 02). Style formalisé dans `G-DESIGN/STYLE.md`.

**Changelog** : ajout de `G-DESIGN/STYLE.md` ; page Jeu passée « validée » dans `PAGES.md`. Prochaine étape : planches Post, Carte de fin, Séries & classement dans ce style (non commencées).

## V1 · déclinaison — 2026-11-18

Planches des 3 pages restantes, dans la continuité stricte de `G-DESIGN/STYLE.md` (même chrome, même maquette, mêmes données de démo) :

- `planches/v1/p1-post.html` — **Post** : splash 512 px dans le feed ; maquette rue éteinte + prévision du soir (« Peak ≈ 20:45 · 70 kW ») + un bouton. États : pas encore joué, déjà joué (95 %, top 3 %), chargement, série cassée.
- `planches/v1/p3-carte-de-fin.html` — **Carte de fin** : % géant + maquette à minuit, lampes éteintes / stock utilisé / rang, courbe complète, histogramme des voisins, accroche commentaire pré-rédigée, prochaine soirée. États : soirée parfaite (rang =1), soirée difficile (recalculée), commentaire posté, première soirée.
- `planches/v1/p4-series-classement.html` — **Séries & classement** : onglets Tonight / My nights (côte à côte sur desktop) ; classement avec ta ligne en bleu, répartition ; série 7, 14 dernières soirées. États : My nights, première soirée, pas encore joué (classement flouté).

**Hypothèses produit** posées pour pouvoir dessiner (Q5, Q6, Q7 + 2 nouvelles) : listées en bas de `G-DESIGN/PAGES.md`.

**Changelog** : +3 planches ; `PAGES.md` : 3 pages « en revue », Jeu « validée », section hypothèses. `/lock` possible dès que ces 3 planches sont validées.

## V1 · LOCK — 2026-11-18

Gaia valide les 3 planches de la déclinaison telles quelles et verrouille le style (`/lock`). **4/4 pages validées** : Post (`p1-post`), Jeu (`03-maquette`), Carte de fin (`p3-carte-de-fin`), Séries & classement (`p4-series-classement`).

La validation vaut aussi pour les choix produit dessinés : un seul geste (maintenir = libérer, relâcher = stocker), prévision visible, coupures = lampadaires éteints (pas de black-out), score = % de rue éclairée, ex æquo départagés par les kWh restés à minuit, une partie par jour, série +1 par soirée jouée, classement flouté avant de jouer, accroche commentaire pré-rédigée.

**Pour le build (opencode)** : référence visuelle = `G-DESIGN/STYLE.md` + les 4 planches ; les planches `01-veillee` et `02-carnet` sont des explorations écartées, à ne pas implémenter. À embarquer dans l'app : une police condensée libre (pas de requête réseau, CSP Devvit).

**Changelog** : `PAGES.md` 4/4 validées ; `STYLE.md` marqué verrouillé.
