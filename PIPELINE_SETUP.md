# Pipeline prospects — mise en place (Google Sheet en direct)

`pipeline.html` est une page **publique en lecture seule** destinée aux prospects.
Elle lit **en direct** une Google Sheet que tu maintiens : tu édites la Sheet →
les prospects voient la dernière version au rafraîchissement, **sans rien renvoyer**.

## 1. Créer la Sheet

1. Nouvelle Google Sheet (sur [sheets.new](https://sheets.new)).
2. Renomme l'onglet en **`Pipeline`** (en bas à gauche).
3. **Ligne 1 = en-têtes**, puis une ligne par deal. Colonnes reconnues
   (l'ordre est libre, les noms tolèrent FR/EN, les colonnes absentes sont ignorées) :

   | Cible | Acquéreur | Secteur | Région | Statut | Annoncé | Closing est. | Contrepartie | Taille $bn | Spread brut | Spread ann. | Note |
   |-------|-----------|---------|--------|--------|---------|--------------|--------------|-----------|-------------|-------------|------|

   - **Taille $bn / Spread brut / Spread ann.** : nombres (le `%` est optionnel, la virgule décimale est acceptée).
   - **Secteur / Région / Statut** deviennent des filtres déroulants.
   - Le fichier `pipeline-sample.csv` de ce repo est un modèle prêt à copier-coller.

## 2. Partager la Sheet en lecture seule

- **Partager → Accès général → Tous les utilisateurs disposant du lien : Lecteur.**
- (Rien d'autre à publier ; la page lit via l'export CSV intégré de Google.)

## 3. Brancher la page

1. Récupère l'**ID** de la Sheet = la partie entre `/d/` et `/edit` dans son URL :
   `https://docs.google.com/spreadsheets/d/`**`CET_ID`**`/edit`
2. Dans `pipeline.html`, remplace `PASTE_YOUR_SHEET_ID_HERE` par cet ID, puis commit/push.
3. Ouvre `https://<ton-user>.github.io/corporate_activity/pipeline.html` → le pipeline s'affiche.

**Test sans éditer le code :** ajoute `?sheet=<ID>` à l'URL de la page.

## 4. Partager aux prospects

Envoie-leur **une seule URL stable** : `…/pipeline.html` (et `…/market-review.html` pour la revue M&A).
Le lien ne change jamais ; seul le contenu évolue quand tu édites la Sheet / republies la review.

## Confidentialité — important

- La Sheet et la page sont **publiques en lecture** : n'y mets **que** ce que les prospects
  peuvent voir. **Pas** de notes internes, positions, tailles réelles ni PDF confidentiels.
- Ton `index.html` (tracker interne complet) reste séparé et n'est pas lié depuis les pages prospects.
- Un lien « non listé » n'est pas secret : quiconque l'a peut l'ouvrir, et il peut être indexé.
