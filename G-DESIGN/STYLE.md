# STYLE — Réseau électrique · direction « Maquette » (validée par Gaia le 2026-11-18)

**VERROUILLÉ le 2026-11-18 (`/lock`)** : fin des explorations ; tout changement de style passe par un re-brief.

Source : `planches/v1/03-maquette.html`. Toute planche suivante reprend ces règles ; une dérive est un défaut.

## Palette (un seul accent)

| Rôle | Hex | Usage |
|------|-----|-------|
| Table (fond) | `#ECEBE6` | fond de jeu, dégradé radial vers `#FBFBF9` au centre et `#E2E1DB` aux bords |
| Fiche | `#FFFFFF` | cartes (courbe, stock, scores) |
| Socle / filets | `#D8D6CE` | bordures 1 px, tranche du socle (`#C6C4BC` face ombrée) |
| Encre | `#111214` | texte, traits, bouton par défaut, manque d'énergie (aplat) |
| Crayon | `#77756E` | libellés, axes, texte secondaire |
| Énergie · **accent** | `#1F63FF` | stock, énergie libérée, lampadaires allumés, curseur « maintenant », bouton actif |
| Fenêtre allumée | `#CFE0FF` | teinte claire de l'accent, seulement dans la maquette |

Interdits : toute autre couleur saturée, dégradé vif, emoji.

## Typographie

- Titres et grands chiffres : linéale très condensée grasse (800, largeur ~62 %), capitales pour le nom du jeu. À embarquer dans l'app : police libre condensée (ex. famille OFL), jamais de requête réseau.
- Données et libellés : mono, capitales espacées 12–16 %.
- Texte courant : linéale système.
- Échelle : 9.5 (libellé) / 13 (texte) / 15 (bouton) / 30 (chiffre) / 36–44 (titre).

## Grille

- Cadre de jeu : marges 16–18 px (mobile), 20–26 px (desktop) ; gouttière 10 px.
- Mobile (390 × 844, référence) : une colonne — titre, maquette (flex), relevés, fiche courbe (104 px), règle, contrôles.
- Desktop (post 736 px) : deux colonnes 1.1fr / 1fr — maquette à gauche sur toute la hauteur, relevés / courbe / contrôles à droite.

## Composants

- **Maquette isométrique** (SVG, angle 30°) : socle 10 × 4.6 avec tranche, ombre au sol elliptique ; maisons blanches à toit encre ; 12 lampadaires (tête blanche éteinte, accent + halo 16 % allumée) ; batterie : niveau en accent sur la face droite, valeur écrite sur la face avant ; câble pointillé accent quand on libère.
- **Fiche courbe** : blanche, rayon 14 px, ombre douce `0 12px 24px -18px rgba(0,0,0,.35)` ; demande passée en encre 2 px, future en pointillé ; production en tirets gris ; énergie libérée en aplat accent ; manque en aplat encre.
- **Relevés** : SUPPLY / DEMAND / GAP, chiffres condensés, unité mono grise ; écart négatif en accent.
- **Stock** : fiche blanche, 10 cellules (accent = plein).
- **Bouton** : rayon 12 px, ≥ 56 px de haut ; encre au repos, accent + ombre bleue quand il est tenu ; sous-libellé mono (« STORE → STREET »).
- **Pastille série** : fond encre, texte mono blanc (« STREAK 06 »).

## Mouvement

- Lampadaires : fondu 240 ms à l'allumage, de gauche à droite.
- Curseur « maintenant » : un quart d'heure par seconde.
- Câble de la batterie : pointillé qui défile tant que le bouton est tenu.
- Ombre au sol de la maquette : suit le niveau de la batterie (respiration lente).
- Aucun rebond, aucune particule.

## États (règles)

Prêt (rue éteinte, prévision seule, bouton « Light the evening ») · Surplus (bouton au repos, batterie qui monte) · Pointe tenue (bouton accent, câble actif) · Stock à sec (lampadaires éteints à partir de la droite, manque en encre sur la courbe) · Déjà joué (courbe complète, bandeau encre « back tomorrow »).
