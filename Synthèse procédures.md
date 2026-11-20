![[_24-25__PaulaA_Stat3_Synth__se.pdf.pdf]]


![[procédures_résumé.pptx]]

--- 
**Données brutes:**
```
data nom_table;
input nom_col_1_alphanumérique $ nom_col_2 nom_col_3;
datalines;
s1 4 5 9   // données séparés par des espaces, pas des "tab"
s2 2 3 10
s3 1 6 9.9    // Décimales avec un '.' (point, pas virgule)

```

`score1-score9`: génère toutes les colonnes entre ces valeurs.

---
**Importer depuis un fichier**
*\*.csv*
```
data nom_de_table;
infile "/home/username/exercice_2/data21.txt" dlm=";" dsd firstobs=2;
informat y1-y7 numx32.; // si nécessaire (voir plus bas)
input col_1 col_2 col_3 ...;
proc print data=nom_de_table;
run;
```
*\*.txt* (pas de délimiteurs)
```
data nom_de_table;
infile "/home/username/exercice_2/data21.csv" firstobs=2; // Si noms de colonnes inclus, sinon commencer à 1
input col_1 col_2 col_3 ...;
proc print data=nom_de_table;
run;
```
*\*xlsx*
Si les noms de colonne sont déjà définies dans le XLSX, utiliser `getnames=yes` et passer l'étape d'après dans laquelle on set les noms manuellement. (Si problème à cette étape, convertir en CSV). 
!! Convertir les valeurs en format US (Excel => format cellules => format Anglais US). 
transforme les décimales à "," en ".", ce que comprend SAS. 
```
proc import datafile="/home/u64611808/Cours_2/data23.xlsx"
    out=data23 dbms=xlsx replace;
    sheet="data23"; // nom de la sheet dans l'excel
    getnames=yes; // Sinon la première rangée servira de titre aux colonnes
run;
proc print data=data23; // out de l'import

// Nécessite de changer soi-même les titres si les colonnes des xlsx sont par défaut A, B, C, ...
data data23;  
	set data23(rename=(A=Nom B=score1 C=score2 D=score3)); 
run;
```
`DLM=";"` délimiteur
`dsd` traite deux délimiteurs contigus comme une donnée manquante
`firstobs` lecture des données à partir de la xième ligne
`informat y1-y7 numx32.;`  avant `input` si les valeurs numériques ont une "," pour les décimales et pas un ".". utiliser `commax32.` pour accepter les . comme séparateurs des miliers.

---
**Remplacer les valeurs vides**
`proc standard data=results mean=0 std=1 out=standardized replace;`
=> Replaces values with `0.0000`

---
**Afficher une table**
`proc print data=nom_table;`
`proc print data=nom_table(obs=15);` limite à 15 le nombre d'observations

**Donner un titre à la table**: 
`title 'Un titre pour ma table';`

**Nouvelle sous-table sur base d'une autre table**
```
data only_females;
	set mixed_genders;
	if Gender='F';
```

**Ajouter une colonne (somme, moyenne etc)**
```
data sum;
	set scores; // Réutiliser la table précédente
		somme = score1 + score2; // col 'somme'
		moyenne_1_2 = mean(score1, score2); // col 'moyenne'
		somme_range = sum(of score1-score8); // ne pas oublier le 'of', sinon c'est un '-' de soustraction
		proc print data=sum;
```

**Ne garder que les colonnes choisies**
```
data sous_ensemble;
	set scores (keep = Nom); // Ne garder que la colonne "Nom"
proc print data=sous_ensemble noobs;
``` 

---
 **proc means**
```
proc means data=sum mean;
	var x y z;
	freq effectifs; // Optionnel, distribution groupée
```
Créé une nouvelle table incluant la moyenne de TOUTES les colonnes à valeurs *numériques*.

Chacun des opérateurs suivants peut être ajouté à la suite de `proc means`. Ex `proc means data=table mean n nmiss ...`
`n` = nombre d'observations
`nmiss` = nombre de valeurs manquantes
`mean` = moyenne
`std` = écart-type
`min` = valeur minimum
`max` = valeur maximum
`var` = variance
`median` = médiane
`mode` = mode
`cv` = corefficient de variation (dispersion)
`alpha=` niveau de certitude, 0.05 par défaut (ex: `alpha=0.05`) - utiliser avec `clm mean std;`
`clm` = interval de confiance sur la moyenne
`range` = étendue
`q1` = premier quartile
`q2` = médiane
`q3` = troisème quartile
`qrange` = intervalle interquartile (q3-q1)
`skew` = indice d'asymétrie (< 0: asymétrie droite. >0: asymétrie gauche)
`kurt` = indice d'aplatissement
`maxdec=` = nombre de décimales souhaitées (souvent 4)
`t` = test $t$ de la nullité de la moyenne
`prt` = probabilité de dépassement du test t
`dispersion` = n'existe pas, utiliser `cv`

*Instructions complémentaires* de `means`
`by`: présenter les résultats en fonction de sous-groupes
`freq`: spécifier la variable de pondération (distribution groupée)

**Sélectionner les variables** sur lesquelles appliquer les opérations (aussi pour **proc print**):
```
proc means data=scores mean;
	var score1 score2 score3;
```
--- 
**proc rank**
```
proc rank data=scores out=sortie descending ties=mean;
	var score1 score2;
	ranks rscore1 rscore2; // créé deux nouvelles colonnes au lieu de remplacer
```
`out=sortie` table de sortie
`descending` décroissant
`ties= mean`; ou `high`, `low`. En cas d'égalité de valeurs, assigne respectivement la valeur `moyenne`, `plus grande` ou `plus petite` valeur de rang;

---
**proc format**
```
proc format;
	value val_to_gender
		1='Femme'
		2='Homme';
	value val_to_level
		1='inf'
		2='moyen'
		3='sup';

data data33_formatted;
	set data33;
	format Genre val_to_gender. Niveau val_to_level.;
```
**Nouvelle colonne conditionnelle**
Ajout d'une colonne sur base de conditions sur d'autres colonnes
```
data entree;
infile: 'C:\path\to\file.csv' dlm=';' dsd firstobs=2;
input ID $ Sexe $ Age ETCV EducEmploi Revenu CESD;
	if Revenu < 10 THEN Revenu2=1;
	if Revenu >= 10 AND Revenu< 20 THEN Revenu2=2;
	if Revenu > 20 10 THEN Revenu2=3;
```
---
 **proc sort**
```
proc sort data=table;
by nom_colonne;
```
---
**proc standard** (Score Z)
```
proc standard data=resultats mean=0 std=1 out=sortie;
	var mes1 temps;
```
---
**proc freq** 
(pourcentages & fréquences cumulés)
"Quel est le nombre de sujets dans la variable x, y?"
"Quel est le pourcentage des sujets entre x >=30?"
```
proc freq data=un;
	tables nom_d'une_colonne;
	weight effectif; // optionnel, porte sur la variable contenant les fréquences
```
---
**proc univariante**
``` 
proc univariante data=un;
	var col_1;
```
Plein de données sur une table. Préciser la colonne sinon on a trop.

---
**intervalles**
```
data un ; 
input binf bsup effectif ; 
	score = (bsup+binf) / 2 ; 
datalines ; 
0 10 12  // où répartition=[0  10] et effectif=12
10 15 17
15 20 23 
20 25 21 
25 30 13 
30 35 10 
35 40 9 
40 50 3 
;
proc print data=un ; run ;
```

---
**meillleur indice de position centrale**
*modalité ordonnée* (faible, bon, satisf, tbon) => médiane => correspond à la valeur qui se situe au milieu de la distribution lorsque les données dont dans l'ordre croissant. 
Si on a des noms de colonne random (ex: bon, très bon etc), on va classer ça à l'oeil:
- 15 participants présentent la modalité "faible" (0-15)
- 13 participants présentent la modalité "satis" (15-28)
- 15 participants présentent la modalité "bon" (28-43 <= 30 est ici)
- 17 participants présentent la modalité "tbon"

La médiane est donc la modalité "bon" car la personne 30 est dans la catégorie "bon".

*modalité nominale*: le mode. 
Correspond à la modalité la plus fréquente. 
=> proc freq + trouver celui qui a la plus grande fréquence (Réponse: A, B, C, ou D).

Note: la moyenne et la médiane portent sur des séries ordonnées, où les données peuvent être rangées. 

Formulations: Attention!!
Quelle proportion: 0 < x < 1;
Quel pourcentage: 0 < x < 100;

*Quelle proportion de l'échantillon a obtenu X > Y et X <Z?*
1) Créer une table avec une colonne 'take' à 1 si la condition est remplie.
2) `proc freq ...;` & `tables take;` Regarder le pourcentage (et mettre en 0.xx si on parle de proportions).