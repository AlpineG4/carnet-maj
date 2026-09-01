# carnet-maj

Canal de mise à jour de l'application **Le Carnet**.

Ce dépôt ne contient que deux fichiers :

- `le-carnet.apk` — la dernière version, signée en debug
- `le-carnet-maj.json` — le manifeste que l'application interroge

Il est public **uniquement** parce que l'application doit pouvoir télécharger
sans jeton. Il ne contient aucune donnée de santé, aucune clé, et aucun code
source : tout cela vit dans le dépôt privé du projet.

Le nom des fichiers est fixe et ne change pas d'une version à l'autre : c'est
ce qui permet à l'URL configurée dans l'application de rester valable.

Ce que le manifeste garantit, et ce qu'il ne garantit pas : l'empreinte
SHA-256 vérifie que le fichier téléchargé est bien celui annoncé ici. La
protection réelle contre un APK substitué est ailleurs — Android refuse
d'installer une mise à jour signée d'une autre clé que celle déjà en place.
