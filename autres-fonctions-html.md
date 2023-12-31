<h1> <font color="#389E46"> Autres fonctions </font> </h1>

<h2>⚔️ Rappel pour le calcul des pourcentages</h2> 

<p>Le calcul d'un pourcentage est différent du calcul d'une réduction ou d'une augmentation.</p>
<p>Pour calculer 10% de 250 €, on doit multiplier par 0,1 : <code>=250*0,1</code> donne 25 €.</p>
<p>Pour calculer une augmentation de 10%, on doit multiplier par 1,1 : <br>
  <code>=250*1,1</code> donne 275 €. <i>(Autrement dit, 1 + 0,1 c'est 100 + 10% d'augmentation, ici 250 + 25) </i> </p> 
<p>Pour calculer une réduction de 10%, on doit multiplier par 0,90 : <br>
  <code>=250*0,9</code> donne 225 €. <i>(Autrement dit, 0,9 ou 1 - 0,1 c'est 100 - 10% de réduction, ici 250 - 25) </i> </p>

<br>

<h2>⚔️ Les fonctions de date </h2> 

<p>Pour rappel, dans l'onglet ACCUEIL, partie <i>Nombre</i>, il est possible de changer le format de la cellule sélectionnée pour lui donner un format de date.<br>
Si, à partir d'une cellule au format de date, on veut isoler dans une autre cellule l'année ou le mois, ou si on veut convertir un numéro de série en année/mois, on utilisera les fonctions suivantes :</p>

<blockquote> <b>=ANNEE(</b> date ou valeur numérique ) <br>
<b>=MOIS(</b> date ou valeur numérique ) </blockquote>

La même formule s'applique pour le <b>JOUR</b>, l'<b>HEURE</b>, la <b>MINUTE</b> et la <b>SECONDE</b>.

<br>

<p>Voici d'autres fonctions de dates utiles :</p>

<blockquote> <b>=AUJOURDHUI()</b> </blockquote>
<p>Renvoie la date du jour. Les parenthèses doivent rester vides.</p>
<blockquote> <b>=JOURS(</b> date 1 ; date 2) </blockquote>
<p>Calcule le nombre de jours entre deux dates.</p>
<blockquote> <b>=NB.JOURS.OUVRES(</b> date 1 ; date 2) </blockquote>
<p>Calcule le nombre de jours ouvrés entiers compris entre deux dates.</p>

<br>

<h2>⚔️ La fonction =TEXTE( </h2> 

<p>Elle permet de convertir un nombre au format texte. Avec différents sigles, on peut composer des formats sur mesure selon nos besoins. </p>
<blockquote> <b>=TEXTE(</b> valeur à convertir ; <b>"</b>format de texte<b>"</b> ) </blockquote>

<p>Les deux sigles importants à rétenir pour utiliser cette formule sont les <code>#</code> et les <code>0</code> : </p>
<ul>
  <li> Un <code>#</code> prévoit l'emplacement d'un chiffre optionnel. </li>
  <li> Un <code>0</code> impose la présence d'un chiffre ; s'il ne dispose pas de chiffre à convertir, un "0" apparaîtra à cet endroit. </li>
</ul>

<p>Voici quelques exemples simples : </p>

<pre>=TEXTE(A1;"0000")</pre>
<p>Cette formule convertit la valeur de la cellule A1 en un texte composé au minimum de 4 chiffres entiers. <br>
Si A1 = 9 alors la fonction affichera <code>0009</code>. Mais si A1 = 42,1 alors elle affichera <code>0042</code>.</p>
<pre>=TEXTE(A1;"#,00")</pre>
<p>Cette formule convertit la valeur de la cellule A1 en un texte contenant un nombre d'au moins deux décimales. <br>
Si A1 = 7,8 alors la fonction affichera <code>7,80</code>. Mais si A1 = 0,6789 alors elle affichera <code>,68</code>.</p>

<br>

<h2>⚔️ La fonction aléatoire </h2> 

<blockquote> <b>=ALEA() </b> </blockquote>
<p>Elle permet de générer un nombre aléatoire entre 0 et 1. Les parenthèses doivent rester vides. <br>
<b>Attention cependant :</b> le nombre aléatoire se régénère à chaque entrée. Pour contourner ce problème, il est possible de copier les valeurs obtenues et d'effectuer un collage spécial de valeurs pour les extraire de la formule.</p>
<blockquote> <b>=ALEA.ENTRE.BORNES( </b> nombre minimum ; nombre maximum )</blockquote>
<p>Cette variante permet de générer un nombre <b>entier</b> aléatoire entre deux bornes choisies.</p>

<br>

<h2>⚔️ Les fonctions d'arrondis </h2>

<blockquote> <b>=ARRONDI(</b> valeur ; nombre de décimales ) <br>
<b>=ARRONDI.INF(</b> valeur ; nombre de décimales ) <br>
<b>=ARRONDI.SUP(</b> valeur ; nombre de décimales ) <br> </blockquote>

<p>Ces fonctions permettent d'arrondir des nombres à virgules. On peut choisir d'arrondir systématiquement à la valeur inférieure ou supérieure.</p>

<br>

<h2>⚔️ La fonction =CONCATENER( </h2>

<blockquote> <b>=CONCATENER(</b> valeur ou formule ou "texte" ; etc. ; etc. ; etc. ) </blockquote>

<p>Celle fonction permet d'assembler dans une même cellule un texte composé de plusieurs éléments, tels que la valeur d'une cellule, le résultat d'un calcul, ou un élément de texte.</p>

<center> <img width=500 src="images/concat.JPG" alt="Exemple 1" /> </center>
<p>Dans cet exemple, on a voulu établir dans la colonne D un code d'identification pour chaque client à partir de sa date d'inscription et selon un format de texte particulier : <code>NOM_ANNEEMOIS</code>. On a utilisé une fonction TEXTE() pour que le mois s'affiche toujours en deux chiffres.</p>
<pre>=CONCATENER(B2;"_";ANNEE(C2);TEXTE(MOIS(C2);"00"))</pre>

<br>
<hr/>
<br>

<center>  <a href="mise-en-forme-conditionnelle-html" target="_self" title="Mise en forme conditionnelle"> <font color="#389E46"> << Mise en forme conditionnelle - Page précédente </font> </a> << • ⚔️ • >> 
  <a href="index-html" target="_self" title="Index"> <font color="#389E46"> Page suivante - Retour à l'index >> </font> </a> </center>
