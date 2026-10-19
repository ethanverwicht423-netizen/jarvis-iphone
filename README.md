# JARVIS pour iPhone — Prototype 0.1

## Ce qui fonctionne
- Interface de chat mobile sombre, style science-fiction
- Historique sauvegardé dans le stockage local du navigateur
- Personnalisation du nom et de la personnalité
- Petite mémoire locale avec la commande « Mémorise que… »
- Lecture des réponses à voix haute si le navigateur la prend en charge
- Dictée vocale via l'API Web Speech si disponible

## Limites importantes
Cette version est un **prototype local**. Elle ne contient pas de véritable modèle d'IA, ne fait pas de recherche Internet et ne se connecte à aucun compte externe. Les réponses sont simulées afin de tester l'interface. La reconnaissance vocale n'est pas prise en charge uniformément par tous les navigateurs iOS.

## Fichiers
- `index.html` : application et styles
- `manifest.webmanifest` : métadonnées d'installation de l'application web

## Utilisation sur iPhone
1. Héberge ces fichiers sur un service HTTPS statique (par exemple GitHub Pages).
2. Ouvre l'adresse HTTPS dans Safari.
3. Appuie sur Partager → Sur l'écran d'accueil.
4. Ouvre JARVIS depuis l'icône créée.

Le simple fait d'enregistrer `index.html` dans Fichiers ne suffit pas pour une installation complète en tant qu'application web.

## Étape suivante : vrai moteur d'IA
Il faudra ajouter un petit backend HTTPS qui appelle un fournisseur de modèle via API. **Ne place jamais une clé API secrète dans `index.html`**, car elle serait visible par toute personne accédant au code. Le backend devra gérer l'authentification, les limites d'utilisation et les données envoyées au fournisseur.

## Confidentialité
Les messages, notes et préférences de ce prototype sont enregistrés dans le stockage local du navigateur. Ils ne sont pas chiffrés par cette application. N'y inscris pas de mots de passe, données bancaires ou informations sensibles. Utilise « Effacer le chat » pour l'historique et « Effacer mémoire locale » pour les notes et préférences.
