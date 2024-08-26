# Javascript

## Mais qu'est ce que ce c'est ?? 

Un language Front-End de développement utilisé afin de rendre le site internet plus dynamique, la gestion des flux des média et inforamtions peu être afficher d emanière dynamique. Il s'atend sur le Back-end grace à la plateforme Node.js qui execute Javascript coté serveur. 

Il est utilisé avec HTML et CSS c'est la base du dévelopement dynamique, sa flexibilité avec l'ensemble des navigateurs web le rend populaire.

En effet, il est executé directement dans le navigateur de l'utilisateur.

## Les termes de base 


- Les variables = Petit conteneur de valeur, elle se déclare avec 5 types principaux: le string, le int, le boolean, le tableau ou l'objet. 
    - Petite spécificité on a 3 appelation pour déclarer une variable: const (99% des cas) et let (1% des cas quand on a besoin de changer la valeur de la variable) et puis var.
- Les operateurs = algébriques( +, -,*,/) op d'assignation (=), d'égalité (===), d'inégalité (!===) ou !(myVariable === 3)
- Les conditons = if, else, else if
- Les fonctions = Elle fait une action que l'on nomme afin de la rappeller ultérieurement, on peu lui appliquer des paramètres (souvent des variables)
- Les evenements = C'est une structure de code que l'on appel lors d'un evenement type le clique, 

## Les ressources qui m'ont bien servies

- MDN web_docs.
- ?? npm ?? // composer ??  




## Les copy/colle de l'exo 

    console.log(`${cities.length} communes chargées`);
    const cl = console.log;
    const db = cities;
    /*
    cities.filter(city => city.population > 300000).sort((a, b) => b.population - a.population).forEach(city => { cl(`Nom: ${city.nom}, Population :${city.population}`) });


    cities.filter(city =>city.codeDepartement === "74").forEach(city => cl(`${city.nom}`));
    */


    // Création d'une fonction getCitiesByDept pour retourner un tableau avec un code postale en paramètre.  

    function getCitiesByDept (cp){
        let cpCities= [];
        db.forEach(db => {if (db.codeDepartement == cp){
            cpCities.push(db)
        }
    });
    return cpCities;
    }
    // utilisation de la fonction dans une vairable afin d'afficher le tableau (ligne 23) et chaque ville (ligne 25).
    let villes = getCitiesByDept("74");
    console.log(villes);

    // création d'une fonction qui affiche les villes du département selectionnée dans getCitiesByDept. 
    
    function displayCity (city){
    villes.forEach(city=>cl(`${city.nom}`));
    }
    displayCity("74");