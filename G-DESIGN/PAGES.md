# PAGES — Réseau électrique

> Statuts : à dessiner / en revue / validée. Liste de départ du brief, **à valider par Gaia**.
> Chaque planche montre le cadre desktop 1440 × 900 et le cadre mobile 390 × 844 côte à côte (brief §6).

| # | Page | Rôle | Contenu clé | Statut |
|---|------|------|-------------|--------|
| 1 | **Post** | Vue dans le feed (splash inline) : donner envie d'allumer le village du soir | En-tête du post, nom du jeu, n° et date de la soirée du jour, série du joueur, bouton d'entrée | à dessiner |
| 2 | **Jeu** | Écran principal, une seule règle : « Hold to send stored power. Let go to save it. » | Courbe de charge du soir (18:00 → 00:00), production vs consommation, curseur « maintenant », jauge de stockage, 12 lampadaires (allumés = demande couverte), un seul contrôle | **validée** · `planches/v1/03-maquette.html` |
| 3 | **Carte de fin** | Résultat + boucle quotidienne + accroche commentaire | Part de la soirée éclairée, coupures, série, invitation à commenter en un geste, prochaine soirée demain | **en revue** · `planches/v1/p3-carte-de-fin.html` |
| 4 | **Séries & classement** | Montrer la série et la communauté | Série perso, scores de la communauté sur la même seed | **en revue** · `planches/v1/p4-series-classement.html` |

États du Jeu montrés en vignettes sur chaque planche V1 : prêt (avant 18:00), surplus (on stocke), pointe (on libère, un lampadaire vacille), déjà joué aujourd'hui.

## Questions produit ouvertes (non tranchées — `IDEE.md` ne dit que « production vs consumption, storage timing »)

1. **Le contrôle** : les planches proposent **un seul geste** (maintenir = libérer le stock ; relâcher = le surplus se stocke tout seul). Alternative : deux boutons Store / Release, ou plusieurs sources à doser. Lequel ?
2. **D'où vient la production ?** Les planches dessinent une production qui baisse au coucher du soleil puis reste à un plancher. Faut-il nommer des sources (soleil, moulin, centrale) ou rester abstrait ?
3. **Prévision** : la courbe de demande future est montrée en pointillé (c'est ce qui rend le timing jouable). On la montre, ou le joueur découvre la soirée en direct ?
4. **Échec** : un manque d'énergie éteint des lampadaires (pénalité) ou met fin à la partie (black-out) ?
5. **Score** : les planches affichent « % de la soirée éclairée » (lit). Autre formule (kWh perdus, coupures) ?
6. **Scores de la communauté** (carte de fin, page 4) : quelle donnée — répartition des % du jour, rang, nombre de joueurs ?
7. **Une partie par jour** ou rejouable (seule la première compte pour la série) ?

## Hypothèses posées dans les planches Post / Carte de fin / Séries (à confirmer ou corriger)

- Q5 : score = % de la soirée éclairée ; ex æquo départagés par les kWh restés en stock à minuit.
- Q6 : voisins = classement du jour (rang + lignes autour de toi) et histogramme des % ; nombre de joueurs affiché.
- Q7 : une partie par jour, pas de bouton rejouer ; la série gagne +1 par soirée jouée, quel que soit le score.
- Nouveau : le classement du jour est flouté tant qu'on n'a pas joué (évite de copier le timing des autres).
- Nouveau : accroche commentaire pré-rédigée (résultat + petite courbe en caractères), postée en un geste.
