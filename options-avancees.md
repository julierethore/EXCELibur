<h1> Les tests logiques </h1>

<h2> ⚔️ La fonction =SI( </h2>

<p>Elle permet d'effectuer un test logique. Si le test est vérifié, la cellule affichera une valeur prédéfinie ; si le test échoue, la cellule affichera une autre valeur.</p>

<blockquote> <b>=SI(</b> test logique ; valeur si VRAI ; valeur si FAUX )</blockquote>

<br>

<center> <img width=200 src="images/fonction_si.JPG" alt="Exemple 1" /> </center>

<center> <i>Exemple 1</i> </center>

<p>Par exemple, pour vérifier si les cellules de la colonne A sont positives ou négatives, on entrera dans la première cellule de la colonne B : </p>
<pre>=SI(A1>0;"Positif";"Négatif")</pre>

<p>Il faudra ensuite "tirer" la cellule pour que la formule s'applique sur toutes les cellules de la colonne B.</p>

<br>
<center> <i>Exemple 2</i> </center>

<p>Je veux savoir si mon semestre est validé. Pour cela, je calcule ma moyenne : c'est mon test logique. Deux résultats sont possibles : soit j'ai la moyenne, doncc le test est réussi, et je valide mon semestre (c'est la valeur si VRAI), soit je n'ai pas la moyenne, donc le test échoue, et je ne valide pas mon semestre (c'est la valeur si FAUX).</p>
<pre>=SI(MOYENNE(A1;A10)>=10;"Semestre validé";"Semestre non validé")</pre>

<br>
<br>

<h2> ⚔️ Les fonctions =ET( et =OU( </h2>

<p>Ces fonctions renvoient "VRAI" ou "FAUX" selon les conditions remplies. Pour la fonction ET, toutes les conditions doivent être remplies pour valider le test. Pour la fonction OU, une seule des conditions est nécessaire.</p>

<blockquote><b>=ET(</b> condition 1 ; condition 2 ; etc. ) <br>
<b>=OU(</b> condition 1 ; condition 2 ; etc. ) </blockquote>

<br>

<center> <img width=500 src="images/fonction_etou.JPG" alt="Exemple 2" /> </center>

<center> <i>Exemple 2</i> </center>

<p>Par exemple, on veut vérifier dans une liste de clients ceux qui ont passé au moins 10 commandes dans la colonne A, <b>et</b> qui ont dépensé plus de 500 € dans la colonne B, <b>et</b> qui ont validé leur inscription dans la colonne C. </p>
<pre>=ET(A1>=10;B1>500;C1="OUI") </pre>
<p>Si on veut vérifier les clients qui n'ont validé aucune de ces conditions, on utilisera cette formule : </p>
<pre>=OU(A1<10;B1<500;C1="NON")</pre>

<br>
<br>

<h2> ⚔️ Les fonctions =SI( imbriquées </h2>

<p>On peut imbriquer dans une fonction SI des formules ET/OU afin de créer des tests plus complexes qui dépendent d'un plus grand nombre de conditions. Ainsi, on utilise la vérification de conditions en "VRAI" ou "FAUX" des fonctions ET/OU pour programmer une fonction SI adaptée.</p>

<blockquote>=SI(ET( condition 1 ; condition 2 ; etc. ) ; valeur si <b>tout est VRAI</b> ; valeur si <b>1 FAUX</b> ) <br>
=SI(OU( condition 1 ; condition 2 ; etc. ) ; valeur si <b>1 VRAI</b> ; valeur si <b>tout est FAUX</b> )</blockquote>

<br>

<p>Dans l'exemple 1, si on veut que les clients ayant rempli **toutes** les conditions aient une réduction de 25% sur leur commande en colonne D, on entrera la formule suivante : </p>
<pre>=SI(ET(A1>=10;B1>500;C1="OUI");D1*0,75;D1)</pre>
<p>Si on veut que les clients remplissant **au moins une** condition aient une réduction de 10%, on utilisera cette formule : </p>
<pre>=SI(OU(A1<10;B1<500;C1="NON");D1;D1*0,90)</pre>

<br>

<p>On peut aussi imbriquer une fonction SI dans une fonction SI pour que le test logique ait trois possibilités de résultats ou plus.</p>

<blockquote>=SI( test logique X ; <b>valeur 1</b> si VRAI ; SI( test logique Y ; <b>valeur 2</b> si VRAI ; <b>valeur 3</b> si FAUX ))</blockquote>

<br>

<p>Dans l'exemple 2, pour vérifier si les cellules de la colonne A sont positives, négatives, ou égales à zéro, on entrera dans la première cellule de la colonne B : </p>
<pre>=SI(A1>0;"Positif";SI(A1=0;"Zéro";"Négatif"))</pre>

<br/>
<hr/>
<br/>

<center> <a href="premiers-pas" target="self" title="Premiers pas"><< Premiers pas - Page précédente</a> << • ⚔️ • >> <a href="mise-en-forme-conditionnelle" target="self" title="Mise en forme conditionnelle">Page suivante - Mise en forme conditionnelle >></a> </center>

