// Process mouton deplacement clavier//
//J'intégre mes variables globales//
//Emplacement départ//
int x = 300;
int y = 300;

//Vitesse deplacement//
int vitesse = 5;

//Ouvrir la console d'affichage//
void setup (){
    // taille de la fenetre//
    size(600,600)
}

//Afficher le refresh (par defaut 60img/sec)//
void draw (){
    //Pour assurer le refresh on met le background dans le Draw//
    background(0,0,0)
      //Puis je vais venir integrer mes fonctions mouton et deplacement//
}

//Fonction d'affichage du mouton//
void mouton(){

    //ici je met la fonction mouton réalisé pendant l'algo//
    //ainsi que la fonction de deplacement//
  

}

//Fonction deplacement clavier//
void goatMove(){
    if(keypressed == TRUE){
        if(keycode == UP){
            y = y - vitesse;
        }
        if(keycode == DOWN){
            y = y + vitesse;
        }
        if(keycode == RIGHT){
            x = x + vitesse;
        }
        if(keycode == LEFT){
            x = x - vitesse;
        }
    }
}

//comme je me connais https://youtu.be/mDOAY93dUNs?si=-G8SMAtlMvJJv4U0 //