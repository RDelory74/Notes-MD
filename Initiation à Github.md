
# Initiation à Github 

en cas de galère : Git Fluence

## Qu'est ce que Git ?? 

Git est un logiciel que l'on installe en locale afin de sauvegarder nos projets, Github et une plateform numérique qui permet de mettre en commun pour le versionnage et le travail en collaboration. 


## Lire les projets

J'ai comparé deux Framework PHP ( fatfree ) et ( symfony ) et si je devais choisir je prendrais le symfony, il présente plus de branches et qui semblent être mise à jour plus recemment. 

La documentation / Les sponsors / le nbr de starzs

L'ajout de starz est utile pour asurer une veille autour d'un projet ou theme, et en plus cela nous affiche les projets starzés par les gens que l'on suit. 

## Les commandes

Dabord j'ai utilisé le terminal pour modifier mon fichier en local et le pousser sur la plateform web. 

plusieurs étapes: 

Je configure le GIt 
git config --global user.name "<Prénom Nom>"
git config --global user.email <adresse-email>
    
    
Je fais le lien avec le repo en ligne
    
    git clone https://github.com/RDelory74/recette-cookies.git  
    
Ensuite J'ai créer un fichier que je modifie (voir command terminal linux) 
    
    Ensuite je grab le fichier
    
    git add "nom du fichier"
    git commit -m "le commentaire"
    git push 
    
    
Enfin j'ai effectuer la même action via mon IDE Visual studio code en naviguant entre source controle et explorer. 
    j'utilise git log pour voir les commits sur mon projet en copier le numéro de commit 
    ensuite avec git checkout + numéro de commit je peux retourner à une version commit antérieur 
    
Je peux constater que les modfications effectué après ont disparues je me retrouve dans un version HEAD détachée qui va me permettre de visionner mon projet à ce niveau ou alors créer une nouvelle branche
    
La commande pour revenir à la dernière version est 
    
    git checkout main 
    
    
Je suis revenur à la dernière version les modifications sont réapparus. 
    
Je découvre aussi la nomenclature des tags, pour créer un tag
    
    git tag 0.1.0
    git push --tags

Les 3 chiffres après le mot tag sont : 
    le premier  0 est la version Majeur //elle evolue si la nouvelle version est incompatible avec l'ancienne 
    le deuxième chiffre est la versio Mineure // Ajoute une fonctionnalité mais toujours compatible
    le troisième chiffre est le patch // corrige les bug sans intervenir sur la compatibilité
    
La staging area est un endroit qui se situe entre git add et le git commit et qui est le fichier dans lequel on fait état du changement ainsi que des actions à commit par la suite. 
    
    git status
Affiche la liste des fichiers modifiers et les fichier qu'il faut ajouter
le repertoire de travail

    git diff
    git diff --base <nom-fichier>
Affiche les conflits d'un fichier

    git reset HEAD <fichier>
Réitinialise l'index (la staging area) d'un fichier
    

 ![merge conflic](/home/rodolphe-delory/Images/Captures d’écran/imprmerge.png "imrpim ecran") 
    
    
    git branch
List l'état des branche et notre position sur celles_ci
    
    git checkout <branch-name>
Nous permet de se deplacer vers la branche citée
    
    git checkout -b <branch-name>
Créé et nous met sur la nouvelle branche
    
    

    



    git rebase <branch-name>
