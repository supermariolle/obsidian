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
infile "/home/username/exercice_2/data21.csv" firstobs=2;
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
`proc means data=sum mean;`
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
`cv` = corefficient de variation
`alpha=` niveau de certitude, 0.05 par défaut (ex: `alpha=0.05`)
`clm` = interval de confiance sur la moyenne
`range` = étendue
`q1` = premier quartile
`q3` = troisème quartile
`qrange` = intervalle interquartile (q2)
`skew` = indice d'asymétrie
`kurt` = indice d'aplatissement
`maxdec=` = nombre de décimales souhaitées (souvent 4)
`t` = test $t$ de la nullité de la moyenne
`prt` = probabilité de dépassement du test t

**Sélectionner les variables** sur lesquelles appliquer les opérations:
```
proc means data=scores mean;
	var score1 score2 score3;
```

 **proc sort**
```
proc sort data=table;
by nom_colonne;
```

---

**proc standard**
```

```