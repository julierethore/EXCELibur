
<h2>Quelques formulations basiques</h2> 


Sélection | Résultat
:-----:|:----
A:A | Toutes les cellules de la colonne A
1:1 | Toutes les cellules de la ligne 1
A1 | La cellule située au croisement entre la colonne 1 et la ligne 1
AI:A10 | Toutes les cellules comprises entre A1 et A10
B1;B3;B8 | Seulement les cellules B1, B3 et B8


Formule | Résultat
:-----:|:----
=C1+C6 | Additionne la valeur de C1 et la valeur de C6
=D4*D5 | Multiplie la valeur de D4 par la valeur de D5
=E7/E2 | Divise la valeur de E7 par la valeur de E2
=SOMME(A1:A10) | Additionne toutes les valeurs des cellules comprises entre A1 et A10
=SOMME(A1:A10;B1) | Additionne toutes les valeurs des cellules comprises entre A1 et A10, plus celle de B1
=MOYENNE(A1:A10) | Calcule la moyenne des valeurs des cellules comprises entre A1 et A10
'=E7/E2 | Affiche « =E7/E2 » en texte dans la cellule sans produire le calcul

--------

<h2> Barre d'outils : onglet ACCUEIL </h2>

<p>Un fichier Excel s’appelle un classeur, et il peut être composé de plusieurs feuilles, ce qui facilite la navigation entre différents tableaux. On peut ajouter des feuilles sur la barre de navigation, en bas. Il est aussi possible de les déplacer pour changer leur ordre, ou de les renommer pour s’y retrouver plus facilement.</p>

<center> <img src="images/feuilles.JPG" alt="Feuilles" /> </center>

-------

<p>En haut, dans l'onglet **Accueil**, la partie *Alignement* permet d'ordonner le texte dans la cellule. <br>
On peut aligner le texte à gauche, à droite, ou au milieu ; en haut, en bas ou au centre de la cellule. <br>
On peut orienter le texte dans différentes direction, et paramétrer un retour à la ligne automatique. </p>

<center> <img src="images/alignement.jpg" alt="Alignement" /> </center>

-------

<p>La partie *Nombre* permet de configurer le format de nombre : ci-dessous, la cellule sélectionnée contient seulement « 1969 » et ce nombre s'affichera différemment en fonction du format choisi.</p>

<center> <img src="images/nombre1.jpg" alt="<- ,OO" /> </center> <br>
<center> <img src="images/nombre.jpg" alt="Nombre" /> </center> <br>
<p>On peut ajuster la quantité de nombres après la virgule à afficher. Par exemple, si on entre dans une cellule « =10/3 », elle s'affiche normalement « 3,3333333 », mais on peut la paramétrer pour qu'elle affiche seulement deux chiffres après la virgule : « 3,33 ». </p>

------

<center> <img src="images/mise_en_forme_conditionnelle.jpg" alt="Mise en forme conditionnelle" /> </center>

<p><b>La mise en forme conditionnelle</b> permet de mettre en évidence les différences de valeurs dans un tableau. Il est important de bien sélectionner la plage sur laquelle s'appliquera la mise en forme avant de la paramétrer. <br>
La plus facile d’utilisation est celle des nuances de couleurs, qui va par exemple colorer les plus petites valeurs en rouge et les plus grandes en vert. Dans « <b>Gérer les règles</b> », on peut personnaliser des règles de mise en forme, notamment pour les cellules contenant du texte. <br>
Plus d'informations [ici](options-avancees). </p>

----------

<center> <img src="images/effacer.jpg" alt="Effacer" /> </center>

<p>Dans la partie <i>Édition</i>, on peut :
- <b>Effacer tout</b> pour vider complètement les cellules
- <b>Effacer les formats</b> pour garder le contenu avec un format par défaut
- <b>Effacer le contenu</b> pour garder le format mais supprimer le contenu

----------

<h3>Trier et filtrer</h3> 

<center> <img src="images/selection_filtre.jpg" alt="Sélection filtre" /> </center>

<p>Pour trier un tableau, bien sélectionner toutes les cellules concernées, afin qu’une colonne ne soit pas triée toute seule sans être accompagnée du reste des informations de chaque ligne. Sur cet exemple, la sélection de cellules est grisée et bordée de vert, et les lignes et colonnes concernées sont foncées.</p>

<center> <img src="images/tri.jpg" alt="Tri personnalisé" /> </center>

<p>Dans « <b>Tri personnalisé</b> », on peut paramétrer les différents niveaux de tri, utiles si certaines valeurs sont identiques dans plusieurs cellules de la même colonne. On peut choisir la colonne, le critère et l’ordre selon lesquels trier le tableau (ci-dessus : tri selon la colonne B, chronologiquement, par ordre croissant).</p>

<p>Pour « <b>Filtrer</b> », il faut sélectionner les colonnes concernées : sur cet exemple, on voit que les colonnes C, D et E sont en foncées en vert, ce qui signifie qu’elles ont été sélectionnées dans leur totalité. En filtrant, un petit curseur va apparaître dans les cellules C1, D1 et E1 : il permet l’affichage d’une liste déroulante des possibilités de filtrage. </p>

> *Remarque :* un tri modifie l’ordre des cellules, et un filtre dissimule des lignes sans les supprimer.

----------

[<< Retour à l'index - Page précédente](index.md) ••• [Page suivante - Options avancées >>](options-avancees.md)











