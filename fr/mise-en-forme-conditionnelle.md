# La mise en forme conditionnelle personnalisée

* [VERSION ANGLAISE](../en/mise-en-forme-conditionnelle.md)
  
## ⚔️ Rappel des bases

![Mise en forme conditionnelle](/images/mise_en_forme_conditionnelle.jpg)

La mise en forme conditionnelle permet de mettre en évidence les différences de valeurs dans un tableau. Il est important de bien sélectionner la plage sur laquelle s'appliquera la mise en forme avant de la paramétrer.

La plus facile d’utilisation est celle des nuances de couleurs, qui va par exemple colorer les plus petites valeurs en rouge et les plus grandes en vert. Dans « <b>Gérer les règles</b> », on peut personnaliser des règles de mise en forme, notamment pour les cellules contenant du texte.

La mise en forme paramètre les cellules concernées selon un format personnalisé. On peut choisir de modifier :

* Le format de nombre (monétaire, pourcentage...)
* La police, la taille, le style d'écriture
* La bordure et le remplissage de la cellule


* * *


## ⚔️ Règles avec formule

Avant de créer une nouvelle règle de mise en forme, il faut veiller à sélectionner toutes les cellules qui seront concernées. On peut choisir d'utiliser une formule afin de déterminer pour quelles cellules (parmi la sélection) le format sera appliqué. <br>



> Formule <code>=$C1=0</code>
>> S'applique à <code>=$A$1:$C$10</code>

Cette formule va chercher dans la colonne C les cellules égales à zéro, et appliquera un format à toutes les lignes correspondantes parmi les 10 sélectionnées, de la colonne A à la colonne C.



> Formule <code>=OU($A1="RETARD";$B1>500)</code>
>> S'applique à <code>=$C:$C</code> 

Cette formule va chercher dans la colonne A les cellules contenant le texte "RETARD", ou dans la colonne B les cellules d'une valeur supérieure à 500, et appliquera un format à toutes les lignes correspondantes dans la colonne C, tant qu'au moins une des deux conditions est remplie.


* * *

<center> <a href="tests-logiques" target="self" title="Tests logiques"> <font color="#389E46"> << Tests logiques - Page précédente </font> </a> << • ⚔️ • >> <a href="autres-fonctions" target="_self" title="Autres fonctions"> <font color="#389E46"> Page suivante - Autres fonctions >> </font> </a> </center>
