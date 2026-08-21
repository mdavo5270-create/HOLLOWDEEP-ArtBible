# HOLLOWDEEP — BIBLE VISUELLE
## Document de référence obligatoire — Jalon Mois 2-3 (cf Document Maître, Partie V.3)

**Statut :** ce document est un contrat avec toi-même. Aucun asset ne doit être intégré au jeu sans avoir été vérifié contre ce document. En cas de doute ou de divergence entre une génération IA et cette bible, **la bible a toujours raison** — on corrige l'asset, jamais la bible sur un coup de tête en cours de production (les révisions de la bible elle-même sont possibles mais doivent être délibérées, cf VBI.7).

**Pourquoi ce document existe séparément du Document Maître :** le Document Maître (Partie IX.13.1) identifie la dérive de cohérence visuelle comme le risque n°1 d'une production solo+IA. Un illustrateur humain maintient un style intuitivement sur la durée ; un outil de génération ne le fait pas sans contrainte externe stricte, réappliquée à chaque session. Ce document EST cette contrainte.

---

## SOMMAIRE

- VBI.1 — Direction artistique générale (style, rendu, contraintes techniques)
- VBI.2 — Palette de couleurs (avec codes exacts, par zone narrative)
- VBI.3 — Fiches de personnages de référence (Talus, l'Archiviste, l'Arpenteur)
- VBI.4 — Fiches de lieux récurrents
- VBI.5 — Gabarits de prompts réutilisables (par type d'asset)
- VBI.6 — Protocole de génération et de contrôle qualité
- VBI.7 — Checklist de cohérence (à passer sur CHAQUE asset avant intégration)
- VBI.8 — Journal d'apport créatif humain (lié à IX.1 du Document Maître)

---

## VBI.1 — Direction artistique générale

### Style retenu

**Illustration peinte semi-stylisée, à la limite entre peinture numérique et gravure.** Références de style à utiliser comme ancrage constant dans chaque prompt (inspiration de rendu uniquement — aucun élément de contenu, personnage ou lieu copié) :
- Textures de peinture visibles, pas de rendu photoréaliste, pas de rendu "concept art AAA" lisse.
- Contraste fort entre zones éclairées (ambre-de-veille, I.3 du Document Maître) et zones sombres — c'est un principe de gameplay autant que de style (la gestion de lumière est une mécanique centrale, II.3.1 type "hotspot caché").
- Traits de contour légers mais présents sur les éléments interactifs (objets, hotspots) — pas sur les éléments de décor pur. Cette distinction stylistique aide involontairement le joueur à repérer intuitivement ce qui est "actionnable" sans que ce soit un bouton explicite (cohérent avec le pilier 1 du Document Maître, Partie 0.2).
- Format de composition : privilégier les compositions verticales ou carrées adaptées au mobile portrait, avec un point focal clair dans le tiers central/inférieur de l'image (zone naturellement la plus regardée sur un écran tenu en main).

### Contraintes techniques

- Résolution de travail : génération en haute résolution puis export optimisé par plateforme (cf Document Maître IX.7, téléchargement à la demande — chaque fond de scène doit rester sous un poids cible d'environ 400-600 Ko compressé après optimisation, à vérifier systématiquement).
- Ratio d'image standard pour tous les fonds de scène : 9:16 (portrait mobile), sauf exception documentée pour des scènes de transition/cinématique.
- Pas d'animation complexe prévue au lancement (cohérent avec le scope contraint établi en Partie V du Document Maître) — les seules animations sont des micro-mouvements de parallax léger (2-3 couches max par scène) et des feedbacks d'interaction (surbrillance, légère pulsation d'un hotspot).

### Ce qu'on évite absolument (rappel du lexique, Annexe E du Document Maître)

Aucune ressemblance visuelle avec l'imagerie Zork identifiable : pas de lanterne de laiton classique façon lampe à huile victorienne trop reconnaissable, pas de silhouette de créature façon "grue", pas de maison blanche, pas de mailbox. La direction retenue ici (gravures, ambre, mécanismes) est délibérément différente visuellement, pas seulement nominalement.

---

## VBI.2 — Palette de couleurs

Palette volontairement resserrée (contrainte de cohérence + coût de génération/retouche maîtrisé, cf Document Maître II.5/V.2).

| Usage | Couleur | Code hex indicatif | Notes |
|---|---|---|---|
| Ambre-de-veille (source de lumière, élément central) | Ambre chaud | `#E8A548` | Couleur signature du jeu — apparaît sur la lanterne, les hotspots actifs, l'UI d'inventaire |
| Ombre / zones non éclairées | Bleu-gris très sombre | `#1B1F2A` | Jamais un noir pur — garder une dominante bleutée pour rester "habité", pas juste vide |
| Pierre / architecture ancienne | Gris chaud | `#8A8378` | Base des décors du Hollow Reach |
| Végétation / éléments organiques (ch.7 Verger de Pierre notamment) | Vert éteint | `#5C6E52` | Désaturé — cohérent avec un lieu "figé", jamais un vert vif |
| Accent narratif (points de bascule, éléments interactifs clés) | Rouille/cuivre | `#B5622E` | Réservé aux objets mécaniques (Talus notamment) et aux éléments liés aux choix majeurs |
| Accent Archiviste (antagoniste ambigu) | Violet froid désaturé | `#5A4E63` | Seule touche de froid contrastant avec l'ambre — signal visuel de son ambiguïté morale |

**Règle stricte :** toute génération d'asset doit inclure ces codes hex explicitement dans le prompt (VBI.5), et toute retouche manuelle doit recaler les couleurs finales sur cette palette avant intégration (VBI.7, item de checklist).

---

## VBI.3 — Fiches de personnages de référence

*(Ces fiches sont les documents à joindre/référencer systématiquement dans chaque session de génération impliquant ce personnage — c'est le principal outil anti-dérive.)*

### Talus — gardien mécanique (chapitre 2, point de bascule #1)

- **Silhouette :** humanoïde massif, proportions trapues (rapport tête/corps volontairement bas pour éviter toute ressemblance avec un archétype de robot générique trop reconnaissable d'un autre média).
- **Matériaux :** corps de pierre ancienne assemblée + articulations et plaques de cuivre/laiton visibles (cohérent avec le puzzle de réparation, II.5 ch.2 du Document Maître).
- **Détail signature :** deux points lumineux au niveau du "visage", couleur ambre (`#E8A548`) à l'état réparé, éteints/gris à l'état désactivé — **cette différence d'état doit être systématiquement présente dans toute scène où Talus apparaît après le chapitre 2**, c'est la traduction visuelle directe du flag `talus_repaired` (Annexe C du Document Maître) et un exemple concret du principe "chapitre de convergence en lecture seule" (II.5 ch.7).
- **Ce qui ne doit JAMAIS varier d'une scène à l'autre :** la forme générale de la tête, la présence des plaques de cuivre, l'échelle relative par rapport à l'Arpenteur (Talus doit toujours paraître imposant mais pas menaçant dans sa posture par défaut).
- **Prompt de référence de base** (à adapter par scène, jamais à réinventer) : *"Gardien mécanique massif, corps de pierre ancienne, articulations et plaques de cuivre visibles, silhouette trapue non-humanoïde-menaçante, [état: yeux ambre allumés #E8A548 / yeux éteints gris selon flag], style peinture numérique texturée, contraste fort ombre/lumière, palette HOLLOWDEEP [joindre VBI.2]"*

### L'Archiviste — antagoniste ambigu (introduit chapitre 4)

- **Silhouette :** longiligne, à l'opposé de Talus (contraste visuel intentionnel entre les deux figures non-humaines/ambiguës du jeu).
- **Détail signature :** vêtements/robe évoquant des pages ou des rubans de texte partiellement effacés — cohérent avec son rôle narratif (gardien de mémoire, cf I.4 du Document Maître).
- **Couleur signature :** violet froid désaturé (`#5A4E63`), seule apparition de cette teinte dans le jeu — renforce son statut de figure à part.
- **Visage :** volontairement partiel/obscurci dans toutes les scènes avant le chapitre 8 (ambiguïté maintenue jusqu'à la finale) — contrainte de composition à respecter strictement, pas seulement une suggestion de style.
- **Prompt de référence de base :** *"Figure longiligne enveloppée de tissus évoquant des pages effacées, visage partiellement obscuré, teinte signature violet froid désaturé #5A4E63 en accent unique, reste de la palette HOLLOWDEEP [joindre VBI.2], style peinture numérique texturée, ambiguïté et retenue dans la posture"*

### L'Arpenteur (protagoniste jouable)

- **Décision de design :** le protagoniste **n'est jamais montré de face ni nommé visuellement de façon détaillée** (vue subjective ou dos/silhouette uniquement, cohérent avec le genre point-and-click à la première personne qui évite le coût de production d'un personnage entièrement animé — décision de scope, pas seulement de style).
- Seul élément visuel constant : la lanterne d'ambre tenue en main, visible en bas de cadre dans les scènes d'exploration — sert aussi de repère UI (jauge de charge visible directement dans la diégèse plutôt que via une barre d'interface séparée, choix d'intégration UX/narratif).

---

## VBI.4 — Fiches de lieux récurrents

*(Les 8 lieux majeurs du jeu, correspondant à la structure narrative I.4 du Document Maître. Chaque fiche est verrouillée avant toute génération de scène s'y déroulant, conformément au protocole VBI.6.)*

### Ravenmoor (chapitre 1 — tutoriel)
- **Chapitre(s) d'apparition :** 1
- **Palette dominante :** gris chaud (`#8A8378`) en base, touches d'ambre (`#E8A548`) sur les fenêtres/lanternes du village, très peu de bleu-gris d'ombre (le village est encore "en surface", à l'inverse du Reach)
- **Éléments architecturaux récurrents :** toits de bois patinés, échoppes basses, la faille elle-même visible en arrière-plan dès les premières scènes (élément d'ancrage géographique constant, rappelle au joueur où mène le récit)
- **État(s) variable(s) selon flags :** aucun — Ravenmoor n'est pas revisité après le chapitre 1, pas de variation à gérer
- **Mots-clés de composition à répéter :** village de bord de faille, lumière de fin de jour, calme avant la descente
- **Asset de référence validé :** à renseigner à la première génération approuvée (jalon Mois 2-3)

### Les Galeries Basses (chapitre 2)
- **Chapitre(s) d'apparition :** 2
- **Palette dominante :** bleu-gris d'ombre (`#1B1F2A`) dominant, percé par l'ambre (`#E8A548`) de la lanterne et les accents rouille/cuivre (`#B5622E`) de Talus et des mécanismes
- **Éléments architecturaux récurrents :** galeries taillées à la main (irrégulières, pas de symétrie parfaite — marque une civilisation plus ancienne et plus artisanale que ce qui suit), rails et poulies abandonnés, présence constante de Talus dans plusieurs scènes (cf VBI.3)
- **État(s) variable(s) selon flags :** aucune variation propre au lieu, mais pose le flag `talus_repaired`/`talus_disabled` qui affecte l'apparence de Talus dans TOUS les lieux suivants où il réapparaît (cf VBI.3)
- **Mots-clés de composition à répéter :** galerie taillée à la main, poulies rouillées, premier contact avec le mécanique
- **Asset de référence validé :** à renseigner

### La Cité Engloutie (chapitre 3)
- **Chapitre(s) d'apparition :** 3
- **Palette dominante :** bleu-gris d'ombre (`#1B1F2A`) avec une teinte plus froide et humide, reflets d'ambre (`#E8A548`) sur les surfaces d'eau stagnante, gris chaud (`#8A8378`) pour l'architecture engloutie
- **Éléments architecturaux récurrents :** colonnes à moitié immergées, mécanismes hydrauliques, verticalité marquée (le seul chapitre à composition majoritairement verticale/en puits, distinct des galeries horizontales du chapitre 2)
- **État(s) variable(s) selon flags :** pose le flag `ch03_water_diverted` — l'état de l'eau ici (avant/après détournement) doit être cohérent avec ce qui sera répercuté au chapitre 7 (Verger de Pierre, cf fiche ci-dessous)
- **Mots-clés de composition à répéter :** immersion partielle, verticalité, reflets, mécanismes hydrauliques anciens
- **Asset de référence validé :** à renseigner

### Le Chœur des Cloches (chapitre 4)
- **Chapitre(s) d'apparition :** 4
- **Palette dominante :** gris chaud (`#8A8378`) et bleu-gris (`#1B1F2A`), première apparition de l'accent violet froid (`#5A4E63`) de l'Archiviste — signal visuel de rupture de ton à ce chapitre
- **Éléments architecturaux récurrents :** cloches et résonateurs de pierre suspendus, architecture verticale ouverte (contraste volontaire avec le confinement des galeries précédentes — le chapitre "s'ouvre" visuellement à mesure que l'intrigue s'élargit)
- **État(s) variable(s) selon flags :** aucun — pas de point de bascule à ce chapitre (cf I.4 du Document Maître, plantation narrative uniquement)
- **Mots-clés de composition à répéter :** résonance, hauteur, première ombre froide (Archiviste), espace ouvert
- **Asset de référence validé :** à renseigner

### Les Marchés Figés (chapitre 5)
- **Chapitre(s) d'apparition :** 5
- **Palette dominante :** rouille/cuivre (`#B5622E`) plus présent qu'ailleurs (anciens étals, enseignes métalliques), gris chaud (`#8A8378`) en base, ambre (`#E8A548`) concentré sur les 2-3 hotspots de faction par sous-zone
- **Éléments architecturaux récurrents :** étals figés en l'état (objets suspendus dans leur dernier usage — signature visuelle du lieu, cohérent avec le nom), trois sous-zones visuellement distinctes mais reliées par une même palette pour ne pas fragmenter la cohérence du chapitre malgré sa structure de hub semi-ouvert (II.5 du Document Maître)
- **État(s) variable(s) selon flags :** pose les flags `faction_a_supported` / `faction_b_supported` — prévoir un léger marqueur visuel (bannière, couleur d'accent) par faction, réutilisé en écho discret au chapitre 8
- **Mots-clés de composition à répéter :** figé en plein usage, marché suspendu dans le temps, choix visible dans le décor
- **Asset de référence validé :** à renseigner

### La Faille Basse (chapitre 6)
- **Chapitre(s) d'apparition :** 6
- **Palette dominante :** bleu-gris d'ombre (`#1B1F2A`) le plus intense du jeu, ambre (`#E8A548`) volontairement rare et précieux (cohérent avec la mécanique de rareté de l'ambre à ce chapitre, I.3 du Document Maître) — la palette elle-même doit "raconter" la tension de gestion de ressource
- **Éléments architecturaux récurrents :** parois brutes non travaillées (on quitte les zones habitées), sensation d'isolement, peu ou pas de vestiges de civilisation
- **État(s) variable(s) selon flags :** un passage alternatif diffère visuellement selon `talus_repaired`/`talus_disabled` (cf II.5 du Document Maître, ch.6) — prévoir les deux variantes de ce passage dès la production, pas en retouche tardive
- **Mots-clés de composition à répéter :** obscurité pressante, rareté de la lumière, isolement, roche brute
- **Asset de référence validé :** à renseigner

### Le Verger de Pierre (chapitre 7 — convergence)
- **Chapitre(s) d'apparition :** 7 (lecture des flags uniquement, aucun nouveau flag posé — cf II.5 du Document Maître)
- **Palette dominante :** gris chaud (`#8A8378`) + vert éteint (`#5C6E52`), touches d'ambre (`#E8A548`) sur les hotspots
- **Éléments architecturaux/naturels récurrents :** arbres pétrifiés, canaux d'irrigation anciens, statues érodées
- **État(s) variable(s) selon flags :** si `ch03_water_diverted = true`, canaux visiblement asséchés et végétation plus grise ; si false, présence d'eau stagnante et touches de vert légèrement plus saturées (jamais vif — reste "figé"). Présence ou absence de Talus selon `talus_repaired` (cf VBI.3, différence d'état des yeux obligatoire)
- **Mots-clés de composition à répéter :** pétrifié, silencieux, symétrie brisée, lumière rasante
- **Asset de référence validé :** à renseigner

### Le Cœur du Reach (chapitre 8 — finale, 3 fins)
- **Chapitre(s) d'apparition :** 8
- **Palette dominante :** variable selon la fin jouée (cf II.6 du Document Maître, score cumulé 0-4) — **Fin Ombre** : bleu-gris (`#1B1F2A`) écrasant, ambre quasi absent ; **Fin Suspendue** : équilibre gris chaud/bleu-gris avec ambre modéré ; **Fin Lumière** : ambre (`#E8A548`) dominant, bleu-gris relégué aux marges du cadre
- **Éléments architecturaux récurrents :** synthèse visuelle des éléments des 7 chapitres précédents (seul lieu du jeu à citer volontairement des motifs déjà vus — galerie taillée, colonne engloutie, cloche — comme échos, pas comme copies)
- **État(s) variable(s) selon flags :** intégralement piloté par le score cumulé (II.6) plutôt que par des flags individuels — un seul asset de base par palier de score (5 variantes, cf VI.2 du Document Maître) plutôt que des combinaisons multiples, cohérent avec la contrainte de production qui a motivé ce choix de design
- **Mots-clés de composition à répéter :** convergence, échos des chapitres précédents, lumière comme verdict
- **Asset de référence validé :** à renseigner

---

## VBI.5 — Gabarits de prompts réutilisables par type d'asset

**Principe : ne jamais écrire un prompt "à la volée" pour un asset de production finale.** Toujours partir d'un des gabarits ci-dessous, complété avec la fiche personnage/lieu correspondante (VBI.3/VBI.4).

### Fond de scène standard
```
[Description de la scène spécifique — action, composition]
+ [mots-clés de composition du lieu, VBI.4]
+ [palette du lieu, sous-ensemble de VBI.2 avec codes hex]
+ "style peinture numérique texturée, contraste fort ombre/lumière ambre,
   composition portrait 9:16, point focal tiers inférieur, sans texte ni interface"
```

### Icône d'objet d'inventaire
```
[Nom et description courte de l'objet, cf Annexe B du Document Maître]
+ "objet isolé sur fond neutre transparent, style cohérent avec illustration peinte HOLLOWDEEP,
   contour léger visible, éclairage ambre directionnel #E8A548, taille lisible en miniature 64x64px"
```

### Personnage récurrent (Talus, l'Archiviste)
```
[Prompt de référence de base de la fiche VBI.3, section personnage concerné]
+ [contexte de la scène spécifique — pose, action]
+ "cohérence stricte avec les apparitions précédentes du personnage, ne pas modifier
   la silhouette, les matériaux ou les proportions établies"
```

---

## VBI.6 — Protocole de génération et de contrôle qualité (lié à IX.13 et V.3 du Document Maître)

1. **Avant toute génération de scène**, ouvrir la fiche de lieu (VBI.4) et, si personnage présent, la fiche personnage (VBI.3). Ne jamais générer "de mémoire".
2. **Génération par lot de 3-4 variantes minimum** par asset, jamais une seule génération acceptée par défaut — la première génération est rarement la plus cohérente avec la bible.
3. **Comparaison immédiate avec le dernier asset validé du même lieu/personnage**, côte à côte, avant toute intégration — c'est le seul moyen fiable de détecter une dérive progressive (VBI.7 formalise cette étape en checklist).
4. **Retouche manuelle systématique** (recalage couleur sur VBI.2, correction de détails hors-bible) — jamais d'intégration d'un export brut sans passage en retouche, même léger (lié à IX.1 du Document Maître : cette étape est aussi ce qui documente l'apport créatif humain).
5. **Archivage du prompt final utilisé et des itérations** dans le dossier de l'asset — alimente VBI.8.

---

## VBI.7 — Checklist de cohérence (à passer sur CHAQUE asset avant intégration au jeu)

- [ ] La palette de couleurs finale correspond aux codes hex de VBI.2 (vérification directe, pas "à l'œil").
- [ ] Si un personnage récurrent est présent, sa silhouette/ses proportions/ses matériaux correspondent à sa fiche VBI.3, comparés côte à côte avec sa dernière apparition validée.
- [ ] Si un lieu récurrent, les éléments architecturaux et l'état de flags correspondent à sa fiche VBI.4.
- [ ] Le style de rendu (peinture texturée, contraste ombre/lumière) est cohérent avec les 3 derniers assets intégrés — pas seulement avec la bible en théorie.
- [ ] Le poids de fichier après optimisation respecte la cible de IX.7 du Document Maître (~400-600 Ko).
- [ ] Une retouche manuelle a bien été appliquée (pas d'export IA brut intégré tel quel).
- [ ] Le prompt et les itérations sont archivés (VBI.8).
- [ ] Aucun élément ne rappelle un élément visuel Zork identifiable (lexique, Annexe E du Document Maître).

**Règle de gouvernance :** un asset qui échoue à 2 items ou plus de cette checklist n'est pas intégré, même si le planning presse — c'est exactement le type d'arbitrage que la Partie V.4 du Document Maître (gouvernance du scope) doit protéger.

---

## VBI.8 — Journal d'apport créatif humain (gabarit, lié à IX.1 du Document Maître)

À tenir pour chaque asset clé (a minima : tous les personnages récurrents, toutes les illustrations de couverture/promotionnelles, les fonds de scène des moments narratifs pivots).

```
Asset : [nom/ID]
Date : [date]
Prompt initial utilisé : [texte complet, gabarit VBI.5 référencé]
Nombre d'itérations : [n]
Modifications manuelles apportées : [recadrage / correction couleur / ajout d'éléments / fusion de deux générations / etc., description précise]
Décisions créatives humaines : [ex. "choix de la pose finale parmi 4 variantes générées, ajustement de la composition pour respecter la règle des tiers, correction de la teinte violette de l'Archiviste hors-modèle vers #5A4E63"]
Outil utilisé et version : [nom de l'outil]
Conditions d'utilisation commerciale vérifiées : [oui/non, date de vérification]
```

Ce journal n'est pas un exercice bureaucratique : c'est la pièce qui permettrait, en cas de contestation future sur la protégeabilité d'un asset (IX.1 du Document Maître), de démontrer une contribution créative humaine substantielle plutôt qu'une génération brute.

---

**Fin de la Bible Visuelle v1.0.**
Ce document doit être finalisé (fiches de lieux complétées, premiers assets de référence validés) avant la fin du jalon Mois 2-3 de la Partie V.3 du Document Maître — aucun chapitre ne doit entrer en production tant que cette bible n'est pas verrouillée sur au moins 3-5 assets tests validés, conformément à V.3.
