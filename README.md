# Crypte Néon — édition GitHub Pages

Cette version est préparée pour être hébergée comme site statique avec GitHub Pages. Le jeu et son code sont intégrés dans `index.html` ; aucune compilation n'est nécessaire.

## Publier le jeu

1. Sur GitHub, crée un dépôt nommé par exemple `crypte-neon-coop`. Avec GitHub Free, rends le dépôt **public** pour utiliser GitHub Pages.
2. Décompresse le dossier si tu utilises l'archive ZIP, puis téléverse **le contenu** du dossier : `index.html`, `README.md` et `.nojekyll` à la racine du dépôt (bouton **Add file → Upload files**).
3. Ouvre **Settings → Pages**.
4. Dans **Build and deployment**, choisis **Deploy from a branch**, la branche `main` et le dossier `/(root)`, puis clique sur **Save**.
5. Quand GitHub affiche l'adresse du site, ouvre-la. Partage cette adresse avec ton ami.

Documentation officielle : https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Jouer en coop à distance

Le jeu possède déjà une connexion WebRTC manuelle. La configuration inclut un serveur STUN public pour améliorer les chances de connexion entre deux réseaux différents ; cela ne garantit pas tous les réseaux.

1. Vous ouvrez tous les deux la même adresse GitHub Pages sur un navigateur récent.
2. Le joueur 1 clique sur **🔗 COOP**, puis **Héberger**. Il copie le code généré et l'envoie au joueur 2 par message privé.
3. Le joueur 2 clique sur **Rejoindre**, colle le code reçu et clique sur **Valider**. Il copie la réponse générée et la renvoie au joueur 1.
4. Le joueur 1 colle cette réponse dans son panneau et clique sur **Valider**. Attendez l'établissement de la connexion.

Gardez les deux pages ouvertes pendant la partie. Le code de connexion est un échange manuel : ne le publiez pas en public.

## Si la connexion ne marche pas

Le réseau ou le pare-feu de l'un des joueurs peut empêcher une connexion WebRTC directe. Dans ce cas, il faut configurer un serveur TURN accessible aux deux joueurs ou mettre en place un serveur de signalisation/relais. GitHub Pages héberge les fichiers statiques, mais n'exécute pas le serveur WebSocket `lan_server.js` évoqué dans le code d'origine.

Ne place aucun mot de passe ou secret de serveur dans un dépôt public.
