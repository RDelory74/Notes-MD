

# PHP (HO YEAHH !!!)

    - PHP: Type de language open source orienté web qui permet de faire le lien entre l'application visuel d'un site et la couche back-end (de manière dynamique). Par son intégration dans le code HTML, il script une information depuis le serveur jusqu'au client.  

## La découverte de l'environnement PHP 

### Glossaire

    - Back end: La couche ou travail les données en arrière plan afin d'attribuer les bonnes informations pour le montage de la structure d'un site.  
    - Front-office: Affichage // Front-end
    - Front end: La couche visuelle, ou se trouve la structure du site. 
    - Back-office: Intégration des données // Front-end

    - Navigateur: Le systéme de navigation sur internet, il permet l'affichage des pages et des informations lorsqu'une url lui est donnée. C'est un client !!! 
    - Le client: C''est le support qui communique avec le serveur. (type un mobile) 
    - Langage client: Il s'agit du langage de programmation (type HTML/CSS/JAVASCRIPT) qui est executé par l'ordinateur du client (de l'utilisateur)
    - Langage compilé: 
    - Langage interprété: 
    - Langage Serveur: Il s'agit du langage qui est traité par un serveur en fonction des requête d'un utilisateur. 

    - Protocole HTTP: C'est le type de transport de l'information depuis le serveur jusqu'au client. 

    - Serveur WEB: C'est un espace de stockage qui supporte les informations pour la conception d'un site. 

      - Les serveurs web les plus connus: 
        - 1 Apache (open source)
        - 2 IIS (Internet Information Server) Microsoft
        - 3 NginX (prononce engineX)
        - 4 Netware (Novell)
        - 5 GWS (Google web server)
  
  
    - Apache: C'est un logiciel de serveur WEB open source, l'un des plus utilisé. 
  
    - Logiciel serveur: C'est un logiciel qui permet de gérer les ressources web d'un serveur web. 
   
    - Front controller: C'est une balise qui permet d'aiguiller les requêtes PHP en fonction des données d'un utilisateur. 




    $ cd ~/public_html
    $ php -S localhost:8000

    https://openclassrooms.com/forum/sujet/texte-dans-echo-apres-variable-28501

    https://apprendre-php.com/tutoriels/tutoriel-6-les-variables.html

    https://blog.crea-troyes.fr/3553/creation-de-layout-en-php-pour-une-mise-en-page-structuree/
    
    https://openclassrooms.com/fr/courses/918836-concevez-votre-site-web-avec-php-et-mysql/912799-ecoutez-la-requete-de-vos-utilisateurs-grace-aux-url


Pour gérer le front controller j'ai utilisé une balise switch sur un fichier index.php, en effet lors du lancement de mon serveur, ce dernier va automatiquement chercher à afficher le fichier index.php, puis avec le code suivant: 

      <?php
      
      $path = isset($_GET['path']) ? $_GET['path'] : '/home';
      
      switch ($path) {
          case '/home':
              include 'home.php';
              break;
          case '/about':
              include 'about.php';
              break;
          case '/chapters':
              include 'chapters.php';
              break;
          default:
              echo "Mais tu t'es planté mec, j'ai pas cette page";
              break;
      }
      ?>
      

Je cré dans un premier temps une variable que j'appelle $path:

    $path = isset($_GET['path']) ? $_GET['path'] : 'home';

Je lui intègre "isset" qui vérifie que la variable est bien déclarée et differente de nulle. 

Puis j'apelle la fonction $_GET qui va récupérer la variable path si elle est présente dans l'URL. 

qui va récupérer l'URI de la page (ligne 60) puis je lance la fonction switch (ligne 62) avec pour paramétre ma variable $path.
Enfin je dis que dans le cas ou l'URI est /home (case'/home') inclure le contenu du fichier home.php (include('home.php')). 
Petite note sur le dernier ou il ne trouverais pas le fichier correspondant à l'URI il affiche un default ('not found php'). 

Je vais faire le même exercie avec une structure If/GET/ELSE/IFELSE: 

    <?php

    $path = isset($_GET['path']) ? $_GET['path'] : 'home';

    if ($path == '/home') {
        include('home.php');
    } elseif ($path == '/about') {
        include('about.php');
    } elseif ($path == '/chapters') {
        include('chapters.php');
    } else echo "404 error php not found !";

    ?>

## Le formulaire

J'ai créé un formulaire avec Chat GPT dans le quel j'ai intégrer les champs et label désirés: 

        <form class="contact-form" action="traitement_formulaire.php" method="POST">
        <label class="form-label" for="civility">Civilité :</label>
        <select class="form-select" id="civility" name="civility">
            <option value="">Sélectionnez votre civilité</option>
            <option value="mr">Monsieur</option>
            <option value="mrs">Madame</option>
            <option value="miss">Mademoiselle</option>
        </select>
        <label class="form-label" for="name">Nom :</label>
        <input class="form-input" type="text" id="name" name="name">

        <label class="form-label" for="email">Email :</label>
        <input class="form-input" type="email" id="email" name="email">

        <label class="form-label" for="Raison">Dans quel but :</label>
        <select class="form-select" id="Raison" name="Raison">
            <option value="">Quel est le but de ton message</option>
            <option value="mr">Je veux changer de Heros</option>
            <option value="mrs">Je veux changer le cours de l'histoire</option>
            <option value="miss">J'ai une super bonne idée</option>
        </select>

        <label class="form-label" for="message">Message :</label>
        <textarea class="form-textarea" id="message" name="message" rows="6"></textarea>

        <input class="form-submit" type="submit" value="Envoyer">
    </form>


Je lui ai attribué une action (me renvoyer sur la page de traitement php traitement_formulaire.php ) et un methode (POST) qui est de récupérer les données

Quand je rempli mon formulaire et que j'appuis sur le bouton Envoyer j'arrive sur uyn page qui m'afiche le resultat suivant: 

array(5) { ["civility"]=> string(2) "mr" ["name"]=> string(6) "Delory" ["email"]=> string(22) "roro_spike@hotmail.com" ["Raison"]=> string(2) "mr" ["message"]=> string(86) "Je trouve que le héros est pas trop trop bien. Je propose que ce soit une héroïne. " }

J'ai bien un tableau à 5 entrées (civility,name,email,Raison,message)

Après je dois le sécuriser avec du PHP sur la partie Front, alors dans mon document de traitement php j'ai mis le code php suivant qui dit que :



        if (strlen($message) < 5) // Si le message a au moins 5 caractères // 
        {
        echo "Le message n'a pas assez de caractères.";
        } 

        if (filter_var($mail, FILTER_VALIDATE_EMAIL)) // si l'email est bien valide
        {
            echo "Félicitation $civilité $name votre requête pour $Raison a bien été envoyée avec le message suivant:$message ";
        } else echo "Le mail n'est pas valide.";
        if (empty($name))  // si le chant name est rempli 
        {
        echo "Le chant Civilité n'est pas valide.";
        } 
        if (empty($Raison)) // si raison est bien selectionner
        {
        echo "Le chant raison n'est pas valide.";
        } 

Code que j'ai réécris de cette façon plus condensé: 

        if (isset($_POST['name']) 
        && isset($_POST['email']) 
        && isset($_POST['message']) 
        && filter_var($_POST["email"], FILTER_VALIDATE_EMAIL) 
        && isset($_POST['civility']) 
        && strlen($_POST['message']) > 5) {
            // Le formulaire a été soumis : récupération des informations et    création des variables

            echo "Félicitation $civilité $name votre requête pour $Raison a bien été envoyée avec le message suivant:$message ";
        }
        else {
            echo "Formulaire pas valide !! ";
            // Le formulaire n'a pas été soumis
            // ...
        }




J'ai créé une fonction qui va protéger mes champs. 

    function valid_info($infos){
    $infos = trim($infos);
    $infos = stripslashes($infos);
    $infos = htmlspecialchars($infos);
    }

Puis je prend soin de l'appliquer à mes variables

     $mail = valid_info($_POST['email']);
     $civilité = valid_info($_POST["civility"]);
     $name = valid_info($_POST["name"]);
     $Raison = valid_info($_POST["Raison"]);
     $message = valid_info($_POST["message"]);








## Super Bonus pour valider les compétences

    Valider la notion de boucle en créant plusieurs images sans répeter le code

    Créer une fonction qui appel notre front controller