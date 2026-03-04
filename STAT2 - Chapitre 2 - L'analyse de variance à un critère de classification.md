![[Psychostat-anov1.pdf]]

L'anova permet de comparer plusieurs groupes (moyennes) avec une seule analyse statistique. 
Permet de comparer plein de groupes 
ET maintenir le taux d'erreurs de première espèce ($\alpha$ = 0.5)
"Y a t-il au moins une différence dans l'ensemble des moyennes sur lesquelles j'ai travaillé?"
$H_0: \mu_1 = \mu_2 = \mu_3$
$H_A$: Toutes les moyennes ne sont pas égales


***Variance vs moyenne?***
On fait une analyse de variance (différent de la moyenne, donc pourquoi analyser les variances): si les moyennes sont toutes égales, c'est qu'il n'y a pas de variabilité entre les moyennes; on va donc calculer une variance sur les moyennes. 
Si la variance entre les moyennes est nulle, c'est qu'il n'y a pas de différences entre les moyennes. 
Si on a 30 scores de stress selon le niveau de responsabilité dans une entreprise (10 par groupe, 3 groupes), on voit qu'il y a de la variabilité. 
Cette variabilité s'expliquer par 2 sources:
- niveau de responsabilité (VI -> VD)
- responsabilité due à l'erreur: d'autres facteurs (facteurs génétiques, psychologie, personnalité, etc)
=> une partie de la variabilité n'est pas explicable.  

**Variance** = moyenne des écarts mis au carré
**Variance** = carré moyen (CM)
**Carré moyen total**: variance calculée sur la totalité des scores

$CM_{\text{erreur}}$ Variabilité liées aux autres facteurs que celui que j'étudie (pas créés par le stress par exemple). Si je calcule la variance à l'intérieur d'un seul groupe, j'exclus la variance attribuée au stress car tous les techniciens ont le même niveau de responsabilité, les cadres ont un autre niveau de responsabilité etc. En restant dans une catégorie, la variabilité n'est pas due au niveau de responsabilité car ils ont tous le même rôle. 

==À effectifs égaux:==
$CM_{\text{erreur}} = \dfrac{\text{variance G1} + \text{variance G2} + \text{...}}{\text{nb groupes}}$
==À effectifs inégaux:==
Formule pondérée

Carré moyen d'erreur: mesure la variabilité sans la variabilité de traitement. Calculé sur des scores individuels
Carré moyen traitement: mesure la variabilité + variabilité de l'erreur. Calculé sur des moyennes.

**Théorème central limite:** la variabilité entre individus est plus élevée que la variabilité calculée sur les moyennes.

$CM_\text{trait} = nx\dfrac{\sum{(\bar{X}_j-\bar{X})^2}}{k-1}$


$F = \dfrac{CM_\text{trait}}{CM_\text{erreur}}$ = 164,24/4 = 35, 06
La variabilité quand on ajoute l'effet du facteur est 35x plus élevée que quand on n'ajoute pas le facteur.

# Calculer l'Anova avec des données brut

1) Facteur de correction
    $FC = \dfrac{\sum{X}^2}{N}$ = 4792/30 = 7648,03
    Note: il ya  souvent des erreurs dans N => ça doit être le N total, de tous les groupes
2) Calculer la $SC_\text{total}$: 
	somme des valeurs au carré - FC
	$(11^2 + 9^2+ ... )$
3) Calculer la SC_trait
4) Calculer la SC_erreur
   SC erreur = SC Total - SC traitement
5) Calculer les degrés de liberté
   $dl_\text{total}$ = N-1
   $dl_\text{trait}$ = k-1 (k=nb catégories)
   $dl_\text{erreur}$ = N-k
6) Calculer CM_trait et CMerreur
7) Calculer le F_obs
8) Chercher la valeur critique
   dl numérateur = dl traitement
   dl dénumérateur = dl erreur

# Si on a les moyennes et les variances
On gagnera du temps pour calculer le carré moyen erreur.
FC, SC gardent la même formule

# Éta-carré
Partie de la variation de la VD expliquée par la VI

$\eta^2 = \dfrac{SC_\text{trait}}{SC_\text{total}}$

Taille de l'effet
Petite: 0,01
Moyenne: 0,06
Grand: 0,14

# Omega-carré
Ajustement du Éta-carré mesure plus précise dans la population. 

# Conditions d'application
- peu de variation de la variance
- normalité

# Pas de conditions d'application?
- La plus grande des variance doit être maximum 4 fois > que la plus petite des variances. 

La transformation logarithmique
La transformation racine carré
La transformation réciproque

**Quand appliquer une transformations?**
hétérogénéité des variances = problème d'égalité des variances
forte asynmétrie

**Kruksal-Wallis**
problème de normalité, avec plus de 2 groupes
- Transformer tous les scores en rangs
- Calculer la somme des rangs pour chacun des groupes


3 groupes:
- Dépresseur
- Stimulant
- Placebo

Si il y a un problème de normalité dans un seul groupe, on a un problème de normalité pour toutes les données.
Dans le groupe Dépresseur, près de 50% des effectifs ont 0.
Dans le groupe Stimulants, près de 40% des effectifs ont 85 (sur 85, le maximum).

On doit donc appliquer le Kruksal-Wallis
On trie dans l'ordre croissant:
0 - 0 - 2 - ...
En cas d'égalité, on fait la somme et on divise par le nb d'items égaux (ici, 0 - 0 => 1 + 2 = 3 => 3/2 = 1,5).

Scores: 0 - 0 - 2 - ...
Rangs: 1,5 - 1,5 - 3

On fait ensuite la somme des rangs pour chacun des groupes.
G1: 35
G2: 115
G3: 40

La distribution khi-carré n'est importante pour nous que pour trouver notre valeur critique dans la table khi-carré selon le degré de liberté avec dl = k-1 où k est le nombre de groupes.

