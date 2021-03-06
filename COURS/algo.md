# Algorithme
-------------

Quand on commence l'apprentissage d'un langage de programmation, il faut commencer par imaginer notre projet de création de programme. 
C'est pourquoi on commence l'apprentissage par le crayon et papier pour se poser une suite de questions. 
C'est le début de la programmation, cela s'appelle de l'algorithme. 

L'algorithme est un ensemble d'actions qui vont évoluer en fonction de la situation. 
En algorithme le programme commence toujours par un début et une fin, c'est pourquoi il est important d'écrire c'est deux mots.

Par exemple décrire toutes les actions pour aller au travail. 

Début
- le réveil sonne
- je me réveille
- je me lave
- je m'habille
- je me coiffe
- je mange 
- je bois
- je mets mes chaussures
- je pars
- j'arrive au travail
Fin

C'est le programme. Maintenant les actions vont être conditionnées par d'autres sous-actions ce qui va permettre l'avancement du programme. 
Par exemple. 

Début
- le réveil sonne ( est-ce que j'ai entendu le réveil ? Oui/non
Fin

Si c'est Oui je peux passer à l'étape suivante, si c'est Non le programme s'arrête là. 
Pour éviter cela, il faut prévoir une étape supplémentaire pour dire :
- le réveil sonne plus fort 

Ainsi de suite. 
C'est des conditions qui s'écrit comme suit :

Début
le réveil sonne,

SI je n'entends pas le réveil

ALORS

--le réveil sonne plus fort

SINON
--Je me réveille

Fin




## Variables
-------------

Les variables sont des espaces de stockage de type mémoire qui permet de sauvegarder un état, des données
durant la vie de notre script (programme). 

Il y a 3 types de variables que l'ont utilisent tout le temps en programmation. 

### Numérique

Permet de stocker des chiffres, nombres entiers, flottant positif et négatif. 


### Alphanumérique

Permet de stocker des lettres, des phrases, des lettres et des nombres. 



### Boolean

Permet de stocker un état positif ou négatif. 
Il est possible de stocker l'état comme suit :
- vrai / faux (true / false)
- 0 / 1


## Déclaration et affectation de variables
----------------------------

Pour déclarer une variable utiliser un nom parlant, pas trop long. Parfois pour les besoins de lecture,
utiliser le camelCase pour éviter les espaces. 
Qui ne commence pas par un chiffre. 
Pour l'affectation d'une variable cela se fait de la gauche vers la droite grâce au signe " = ". 
L'affectation de chaînes de caractères se fait à l'intérieur de guillemets. 


myVariable = 123
age = myVariable - 100       // age vaut 23
name = "Marsouins"


## Conditions

Nous l'avons vu plus haut. La construction de la condition
SI quelque chose n'est pas réalisée
ALORS réaliser cette chose
SINON passer à la chose suivante

Pour tester les différentes actions, nous utilisons des opérateurs. 
- = égal à
- `< strictement plus petit que`
- `> strictement plus grand que`
- `<= inférieur ou égal à`
- `>= supérieur ou égal à`

- <> ou != Différent de
- & ET
- | OU
 

Comment vérifier si j'ai l'âge requis pour être Marsouins. 

Il faut pour cette exemple 2 variables
- ageM = 26
- myAge = 20

SI myAge > ageM ALORS
Je ne peux pas être Marsouins
SINON
Je peux être Marsouins


## Boucle

La boucle est une suite de tests pour vérifier l'état d'une action pour vérifier que celle-ci soit vrai. 

TANTQUE cette action n'est pas vrai
FAIRE ajouter +1
FIN TANTQUE arrêter action

Je vais utiliser les mêmes variables de l'exemple précédent. 
- ageM = 26
- myAge = 20

TANTQUE myAge < ageM
FAIRE myAge + 1
FIN TANTQUE




## Tableaux

Pour stocker en ensemble d'informations qui concerne la même variables, l'utilisation d'un tableau est très utile. 
Pour déclarer un tableau :
- monTableau = []

A l'intérieur il est possible de stocker des chaînes de caractères et des nombres. 
Affections de données dans un tableau de fait comme suit :

- monTableau = ["Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi"]
- autreTableau =[1,2,3,4,5]

Pour afficher une valeur précise d'un tableau, il faut appeler le tableau par l'index de la valeur souhaitée. 
**ATTENTION** en algorithme l'index de tableau commence par 1 mais en utilisant un langage de programmation, l'index d'un tableau commence par 0.

monTableau[2] affiche la valeur "Mardi"
autreTableau[4] affiche la valeur 4

En JavaScript par exemple la lecture du tableau donne ceci :

monTableau[2] affiche la valeur "Mercredi"
autreTableau[4] affiche la valeur 5

Pour lire l'ensemble des valeurs d'un tableau, on utilise une boucle. 
Il faut compter le nombre d'éléments dans un tableau, ce nombre sera la limite de lecture du tableau. 

Il faut déclarer une variable pour déclencher la boucle. 



## Fonctions

Les fonctions sont très pratiques pour mettre en place des algorithmes répétitif et permet une écriture plus courte. 
Dans certains langages de programmation, des fonctions existent, il suffit juste de les appeler. 

Par exemple une fonction connue est celle d'afficher une date :
- date()     // affiche la date du jour

Cette fonction peut aussi accepter des paramètres. Par exemple, je veux afficher l'année uniquement. 
- date("Y")  // affiche 2019

On peut aussi créer des fonctions pour réaliser des actions correspondant à nos besoins. . 

Par exemple déclararer une fonction "calculer" pour effectuer une addition et afficher le résultat. 

FONCTION calculer(parametre1, parametre2)
{
  // Faire une addition et sauvegarder résultat
  total = parametre1 + parametre2

  // Afficher résultat
  AFFICHER total

}

Pour exécuter la fonction et passer des nombres en paramètre il faut faire ceci :
calculer(400, 560)

Le résultat sera 960. 


## Mettre en pratique

A partir de tout les éléments vus ici, seriez-vous capable d'écrire une fonction "aller_au_travail()"?
A vous de jouer. 


## pour vous entraîner


Exercice en ligne

https://www.kwyk.fr/algorithme/fonction/

https://www.kwyk.fr/algorithme/problemes2/
