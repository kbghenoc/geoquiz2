# GeoQuiz — Le terrain du savoir

Prototype de quiz géologique en **HTML, CSS et JavaScript vanilla**, conçu pour être hébergé sur GitHub Pages.

## Fonctionnalités
- Profil local avec création de compte et connexion sur le même navigateur.
- 10 domaines des géosciences : géologie générale, géologie pétrolière, pétrophysique, sédimentologie, géologie structurale, minéralogie/pétrographie, hydrogéologie, géophysique, cartographie/SIG et géochimie/environnement.
- Trois niveaux de difficulté, formats de 5/10/15 questions et chronomètre configurable.
- Ordre des questions et des réponses mélangé à chaque session.
- Points, bonus de rapidité, bonus de série, correction expliquée, historique et classement local.
- Interface responsive pour ordinateur, tablette et mobile.

## Lancer localement
1. Décompresse le dossier.
2. Ouvre `index.html` dans un navigateur moderne.
3. Pour un environnement local plus proche d'un hébergement web, ouvre un terminal dans ce dossier et lance :
   ```bash
   python -m http.server 8000
   ```
   Puis ouvre `http://localhost:8000`.

## Publier sur GitHub Pages
1. Crée un dépôt GitHub, par exemple `geoquiz`.
2. Ajoute `index.html`, `style.css`, `app.js` et `README.md` à la racine du dépôt.
3. Dans **Settings → Pages**, choisis la branche principale (`main`) et le dossier `/ (root)`.
4. Enregistre et attends la publication. GitHub affichera l'adresse du site.

## Important — limites de la version statique
Cette version ne nécessite aucun serveur et peut être hébergée gratuitement sur GitHub Pages. En revanche, les comptes, mots de passe hachés et scores sont stockés **uniquement dans le navigateur** (`localStorage`). Ce n'est pas une authentification sécurisée : les données peuvent être effacées, modifiées ou perdues, et le classement n'est pas partagé entre participants ou appareils.

Pour un vrai concours public, il faudra ajouter une API/backend (par exemple Django ou FastAPI), une base de données, une authentification sécurisée, des règles anti-triche et un classement serveur. Ne pas utiliser cette démo pour stocker des données sensibles.


## Banque de questions enrichie

La version enrichie structure le quiz en **10 domaines × 10 niveaux × 10 questions = 1 000 entrées de quiz**. Chaque domaine affiche 100 questions et chaque niveau propose 10 entrées par domaine. Les niveaux progressent des fondations à la maîtrise, avec points adaptés au niveau.

**Note pédagogique :** cette banque est une première version structurée à valider par un enseignant ou géologue référent avant utilisation dans un examen officiel. Les scénarios sont progressifs, mais certains thèmes fondamentaux reviennent entre niveaux ; une prochaine révision peut remplacer ces récurrences par 1 000 questions entièrement rédigées et vérifiées individuellement.
