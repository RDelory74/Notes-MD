//Process pour créer un repo depuis un projet créé en local.//

 Dans VS Code (Terminal > Nouveau terminal).

Initialise le dépôt Git local (si ce n'est pas déjà fait) :

  git init

Ajoute tous tes fichiers :

  git add .

Fais un premier commit :

  git commit -m "Initial commit"

Crée un nouveau dépôt vide sur GitHub :

Va sur GitHub.
Clique sur New repository.
Ne coche rien (pas de README, pas de .gitignore, pas de licence).

Copie l’URL du repo, genre : https://github.com/ton-utilisateur/nom-du-repo.git


Ajoute ce repo distant à ton projet :

  git remote add origin https://github.com/ton-utilisateur/nom-du-repo.git


Push ton projet sur GitHub :

  git branch -M main
  git push -u origin main

Et voilà  !
