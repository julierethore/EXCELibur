<h1> <font color="#389E46"> La mise en forme conditionnelle personnalisée </font> </h1>

<h2>⚔️ Rappel des bases</h2>

<center> <img width=500 src="images/mise_en_forme_conditionnelle.jpg" alt="Mise en forme conditionnelle" /> </center>

<p>La mise en forme conditionnelle permet de mettre en évidence les différences de valeurs dans un tableau. Il est important de bien sélectionner la plage sur laquelle s'appliquera la mise en forme avant de la paramétrer. </p>
<p>La plus facile d’utilisation est celle des nuances de couleurs, qui va par exemple colorer les plus petites valeurs en rouge et les plus grandes en vert. Dans « <b>Gérer les règles</b> », on peut personnaliser des règles de mise en forme, notamment pour les cellules contenant du texte. </p>
<p>La mise en forme paramètre les cellules concernées selon un format personnalisé. On peut choisir de modifier : </p>
<ul>
  <li>Le format de nombre (monétaire, pourcentage...)</li>
  <li>La police, la taille, le style d'écriture</li>
  <li>La bordure et le remplissage de la cellule</li>
</ul>

<br>
<hr />

<h2>⚔️ Règles avec formule</h2>

<p>Avant de créer une nouvelle règle de mise en forme, il faut veiller à sélectionner toutes les cellules qui seront concernées. On peut choisir d'utiliser une formule afin de déterminer pour quelles cellules (parmi la sélection) le format sera appliqué. <br>

<br>

<blockquote> Formule <code>=$C1=0</code> <br>
<blockquote>S'applique à <code>=$A$1:$C$10</code> </blockquote> </blockquote>
<p>Cette formule va chercher dans la colonne C les cellules égales à zéro, et appliquera un format à toutes les lignes correspondantes parmi les 10 sélectionnées, de la colonne A à la colonne C.</p>

<br>

<blockquote>Formule <code>=OU($A1="RETARD";$B1>500)</code> <br>
<blockquote>S'applique à <code>=$C:$C</code> </blockquote> </blockquote>
<p>Cette formule va chercher dans la colonne A les cellules contenant le texte "RETARD", ou dans la colonne B les cellules d'une valeur supérieure à 500, et appliquera un format à toutes les lignes correspondantes dans la colonne C, tant qu'au moins une des deux conditions est remplie.</p>


<br>
<hr/>
<br>

<center> <a href="tests-logiques-html" target="self" title="Tests logiques"> <font color="#389E46"> << Tests logiques - Page précédente </font> </a> << • ⚔️ • >> <a href="autres-fonctions-html" target="_self" title="Autres fonctions"> <font color="#389E46"> Page suivante - Autres fonctions >> </font> </a> </center>
