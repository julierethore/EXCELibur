# Autres fonctions

* [ENGLISH VERSION](../en/autres-fonctions.md)
  
## ⚔️ Rappel pour le calcul des pourcentages

Le calcul d'un pourcentage est différent du calcul d'une réduction ou d'une augmentation.

Pour calculer 10% de 250 €, on doit multiplier par 0,1 : <code>=250*0,1</code> donne 25 €.

Pour calculer une augmentation de 10%, on doit multiplier par 1,1 : <br>
  <code>=250*1,1</code> donne 275 €. *(Autrement dit, 1 + 0,1 c'est 100 + 10% d'augmentation, ici 250 + 25)*

Pour calculer une réduction de 10%, on doit multiplier par 0,90 : <br>
  <code>=250*0,9</code> donne 225 €. *(Autrement dit, 0,9 ou 1 - 0,1 c'est 100 - 10% de réduction, ici 250 - 25)*

* * *

## ⚔️ Les fonctions de date

Pour rappel, dans l'onglet ACCUEIL, partie *Nombre*, il est possible de changer le format de la cellule sélectionnée pour lui donner un format de date.

Si, à partir d'une cellule au format de date, on veut isoler dans une autre cellule l'année ou le mois, ou si on veut convertir un numéro de série en année/mois, on utilisera les fonctions suivantes :

> **=ANNEE(** date ou valeur numérique ) <br>
> **=MOIS(** date ou valeur numérique ) 

La même formule s'applique pour le **JOUR**, l'**HEURE**, la **MINUTE** et la **SECONDE**.



Voici d'autres fonctions de dates utiles :

> **=AUJOURDHUI()**

Renvoie la date du jour. Les parenthèses doivent rester vides.

> **=JOURS(** date 1 ; date 2 )

Calcule le nombre de jours entre deux dates.

> **=NB.JOURS.OUVRES(** date 1 ; date 2 )

Calcule le nombre de jours ouvrés entiers compris entre deux dates.

* * *

## ⚔️ La fonction =TEXTE(

Elle permet de convertir un nombre au format texte. Avec différents sigles, on peut composer des formats sur mesure selon nos besoins.

> **=TEXTE(** valeur à convertir ; **"**format de texte**"** ) 

Les deux sigles importants à rétenir pour utiliser cette formule sont les <code>#</code> et les <code>0</code> :

* Un <code>#</code> prévoit l'emplacement d'un chiffre optionnel. 
* Un <code>0</code> impose la présence d'un chiffre ; s'il ne dispose pas de chiffre à convertir, un "0" apparaîtra à cet endroit.


Voici quelques exemples simples :

~~~
=TEXTE(A1;"0000")
~~~

Cette formule convertit la valeur de la cellule A1 en un texte composé au minimum de 4 chiffres entiers. <br>
Si A1 = 9 alors la fonction affichera <code>0009</code>. Mais si A1 = 42,1 alors elle affichera <code>0042</code>.

~~~
=TEXTE(A1;"#,00")
~~~

Cette formule convertit la valeur de la cellule A1 en un texte contenant un nombre d'au moins deux décimales. <br>
Si A1 = 7,8 alors la fonction affichera <code>7,80</code>. Mais si A1 = 0,6789 alors elle affichera <code>,68</code>.


* * *

## ⚔️ La fonction aléatoire

> **=ALEA()**

Elle permet de générer un nombre aléatoire entre 0 et 1. Les parenthèses doivent rester vides. <br>
**Attention cependant :** le nombre aléatoire se régénère à chaque entrée. Pour contourner ce problème, il est possible de copier les valeurs obtenues et d'effectuer un collage spécial de valeurs pour les extraire de la formule.

> **=ALEA.ENTRE.BORNES(** nombre minimum ; nombre maximum )

Cette variante permet de générer un nombre <b>entier</b> aléatoire entre deux bornes choisies.

* * *

## ⚔️ Les fonctions d'arrondis

> **=ARRONDI(** valeur ; nombre de décimales ) <br>
> **=ARRONDI.INF(** valeur ; nombre de décimales ) <br>
> **=ARRONDI.SUP(** valeur ; nombre de décimales )

Ces fonctions permettent d'arrondir des nombres à virgules. On peut choisir d'arrondir systématiquement à la valeur inférieure ou supérieure.

* * *

## ⚔️ La fonction =CONCATENER(

> **=CONCATENER(** valeur ou formule ou "texte" ; etc. ; etc. ; etc. )

Celle fonction permet d'assembler dans une même cellule un texte composé de plusieurs éléments, tels que la valeur d'une cellule, le résultat d'un calcul, ou un élément de texte.

<center> <img width=500 src="images/concat.JPG" alt="Exemple 1" /> </center>

Dans cet exemple, on a voulu établir dans la colonne D un code d'identification pour chaque client à partir de sa date d'inscription et selon un format de texte particulier : <code>NOM_ANNEEMOIS</code>. On a utilisé une fonction TEXTE() pour que le mois s'affiche toujours en deux chiffres.

~~~
=CONCATENER(B2;"_";ANNEE(C2);TEXTE(MOIS(C2);"00"))
~~~

* * *

<center>  <a href="mise-en-forme-conditionnelle" target="_self" title="Mise en forme conditionnelle"> <font color="#389E46"> << Mise en forme conditionnelle - Page précédente </font> </a> << • ⚔️ • >> 
  <a href="index" target="_self" title="Index"> <font color="#389E46"> Page suivante - Retour à l'index >> </font> </a> </center>
