# HTML/CSS

On créé un fichier html qu'on met en lien avec un fichier CSS 
On donne la nature de la fiche puis les caractéristiques et propriété de la page: 

<!DOCTYPE html>
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link
        href="https://fonts.googleapis.com/css2?family=Alegreya+Sans+SC:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&display=swap"
        rel="stylesheet">
    <link rel="stylesheet" href="member.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css">
    <title>Alpina Avenue</title>
</head>



Les balises 
<body>
<main>
<header> // <footer>
<section>
<div>
<p>
<img>	"alt"
<a>	"href"

<h1/2/3>


background-size
si tu mets une image tu peu utiliser no-repeat pour pas qu'il repete l'image à l'infini. 
background: url(

pour positionner=

padding (left/right/up/down) 
ou margin (left/right/up/down)

iframe= balise qui permet de generer une fenetre pour une lecture video

Flexbox (Bootstrap) = intégration des fonction Flexbox directement en ajoutant des classes dans le HTML type d-flex: pour les containers puis align-self pour les elements indépendants.

Flexbox= rendre une boite (container or div) flex, puis lui appliquer une orientation sur deux axes cross pour la hauteur et main pour la longueur, 

Donc 2 façons de disposer la direction des box, le type "row", par defaut en ligne, et column en colonne après on vient modifier le row dans une colonne avec justify-content et dans le row avec le align-content
bref pour plus d'infos voir cette vidéo: 

https://youtu.be/wrRd1W_vtUw?feature=shared

Les selecteurs:
espace: selectionne tous les elements d'une nature d'une classe peu importe le niveau

		ex: 

	main p{
		}

+: sélectionne le premier element enfant dans une balise qui suit une balise de type 

ex: 

	main img + p{}

cela va concerner le premier texte suivant une balise image et ce pour toutes les balises image. 

~: même principe que pour le + sauf que dans ce cas il s'agit de l'élements qui précède une balise. 

enfin le chevron qui lui va selcetionner tous les elements d'un type (genre p ou img) de premier niveau. 



Bootstrap: 

Enfin je dirais que bootstrap est un framework que l'on appel via un lien dans le head de notre html. 

en faisant ce lien on fait appel à tous le css de bootstrap ce qui nous permet d'intégrer des elements en les appellant simplement ou alors de la modifier en ajoutant des class(respecter la nomenclature de boostrap) via un espace 

ex: 

<p class="w-50 bg-dark d-flex flew-direction:column justify-content:center>

w-50 c'est la largeur w=widht	bg-dark c'est la couleur de background d-flex c'est l'aplication du contenu flex dans la class.

Enfin le fait de travailler le css seulement sur le html au travers d'un framework on appel ça l'utility first.









