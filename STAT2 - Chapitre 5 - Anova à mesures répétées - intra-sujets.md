
![[Anova mesure répétées.pdf]]
Définition: **==Anova à mesures répétées: extension test t pour échantillons pairés==**
Anova: Analyse de la variance

Exemple d'uitlisation:
Étude pour comparer 3 méthodes d'enseignement. Mais je sais que mes étudiants ont un QI très variable. Je divise ensuite les enfants en 3 groupes selon leur QI mesuré, pour 


On prend des sujets, on les rend identiques sur les variables étudiées (on efface les variables interindividuelles) pour obtenir une variabilité résiduelle et pouvoir tester l'effet d'une VD sur une VI. 
On distingue la variabilité intra-sujets et inter-sujets et on neutralise la variabilité inter-sujets.
La variabilité inter-sujets est plus grande que la variabilité intra-sujets (on ne varie pas avec soi-même). 
Comment neutraliser la 

Exemple: on fait une étude pour étudier les compétences des élèves en arithmétique au cours de l'année (4 tests pour tester l'évolution). 
On teste les mêmes sujets à 4 moments différents.
VD: nb de réponses correctes sur /50



| Sujet   | Test 1 | Test 2 | =test 3 | Moyenne |
| ------- | ------ | ------ | ------- | ------- |
| 1       | 2      | 4      | 6       | 4       |
| 2       | 10     | 12     | 17      | 13      |
| 3       | 20     | 23     | 26      | 23      |
| 4       |        |        |         | 43      |
| Moyenne | 18     | 20,75  | 23,5    |         |
|         |        |        |         |         |



Variance très grande car on a forcé des bons et mauvais résultats pour l'exemple. 
On veut voir la différence à travers les sujets eux-mêmes. Comment un sujet évolue?
Comme ce qui caractérise les sujets est qu'ils ont une très grande différence entre eux, est-ce que je ne pourrais pas modifier les résultats des élèves pour les ramener vers une moyenne égale? 
Dans les faits, c'est tricher mais mathématiquement, on peut:
On remet les moyennes de tous les élèves à 23 MAIS on adapte leurs scores pour garder les différences entre chaque score.
Sujet 1: moyenne de 4 -> 23 => je prends chaque score et je rajoute 19 aux scores aussi
Sujet 1: 21 : 23 : 25 : 23 (moyenne).
Pourquoi 23 ? C'est arbitraire pour l'exemple.
**Dans les faits, on met la moyenne à 0, pas à 23!**



| Sujet    | Test 1 | Test 2 | =test 3 | Moyenne |
| -------- | ------ | ------ | ------- | ------- |
| 1        | -2     | 0      | 2       | 0       |
| 2        |        |        |         | 0       |
| 3        |        |        |         | 0       |
| 4        |        |        |         | 0       |
| Moyenne  | -2,75  | 0      | 0,25    | 0       |
| Variance | 0,25   | 0,67   | 0,92    |         |
On a donc supprimé la variabilité inter-individuelle; on ne voit plus que la varaibilité intra-individuelle, donc l'évolution de chacun à travers les tests

Je prends les 4 moyennes des 4 groupes, les 4 variances

Étape 1: 
Calculer le facteur de correction
$DC = \dfrac{\sum{X}^2}{N}$ où N est le nombre d'observations total (toutes les observations de tous les individus). 

SC_total = $\sum{X}^2 - {FC}$ (d'abord mettre au carré puis les additionner). où FC est le facteur de correction. 

Etape 4: 
SC_sujets

Etape 5: 
SC_erreur: SC_total - SC_A - SC_sujets

N = nb d'observation
n = nb de participants


Plans d'ordre supérieur
Les mêmes participants passent dans toutes les cellules. 

# 2 conditions d'application pour les anova mesure répétées

# **==condition de sphéricité==**
On ne sait pas le voir à l'oeil nu, on demande généralement à un ordinateur. 
Solution: procédure simple permettant de la contourner OU problème de sphéricité mentionné dans l'énoncé de l'examen.

Anova à mesures répétées: extension test t pour échantillons pairés.
Pour les tests t pour échantillons pairés, on faisait la moyennes des différences T1 /  T2.
Condition: ==La variances des scores de différences ne doit pas être trop éloignées les unes des autres==. On devrait donc calculer la variance pour chaque paire puis les comparer les unes aux autres. 

Homogénéité des variances des scores de différence

## Violation de la condition de sphéricité
2 solutions:
1) Adaptation du degré de liberté
2) Analyse multivariée de la variance (MANOVA)

Quand il y a un pb de sphéricité, on sait adapter (diminuer) le degré de liberté pour obtenir une valeur critique plus sévère (plus grand).

Il faut calculer un epsilon ($\epsilon$), valeur entre 0 et 1 qui va servir à multiplier notre degré de liberté (et donc le réduire, car c'est une valeur entre 0 et 1). 

$dl = (a-1) * \epsilon$ 
$dl_{erreur} = (a-1)*(n-1)*\epsilon$


Pire solution
$dl_A=1$
$dl_{erreur} = n-1$

**Significatif = $H_0$ est rejeté**
**Non-significatif = $H_0$ non rejeté**
Si l'effet n'est pas significatif avec des degrés de liberté gentils, on n'a pas besoin d'aller plus loin.
Si l'effet est significatif avec des degrés de liberté gentils, on peut augmenter la sévérité des degrés de liberté (mettre $dl_A$ à $1$ et $dl_{erreur}=n-1$) et si ça reste significatif, on peut affirmer que l'effet est bien significatif. 

## Violation de la condition de normalité
Test non paramétrique de Friedman. Fonctionne avec une seule variable indépendante dans les tests à mesure répétées. 

Test basé sur des rangs **pour chaque sujet pris séparément**.
Le test ne fonctionne pas avec des ex-aequo. 

Rangs: on attribue à un score sa position si on avait trié les scores dans l'ordre croissant:
Scores: 10, 14, 19, 22 => Rangs: 1, 2, 3, 4
3, 8, 6, 1 => 2, 4, 3, 1

k = nombre de conditions
R_i = somme des rangs
N = sombre total de sujets dans l'étude (9 enfants: N = 9)

Dans la formule: 12 c'est 12, 3 c'est 3.

On cherche la valeur critique dans la table Khi carré avec
$dl = k-1$
$\chi_{0,05}(3) = 7,85$ (ou qq chose de cet ordre)


Attrition - problème des effectifs inégaux
Si un participant n'est pas venu à toutes les séances, on aura peut-être 4 scores sur 5. Dans ce cas, on peut:
- supprimer toutes les données de ce participant (préféré)
- estimer les scores restants


# MANOVA (pas à connaitre)
Analyse multivariée de la variance. Analyse de variance dans lesquelles on a plusieurs variables dépendantes en même temps. 
Pas de conditions d'application. 
Exemple: 
3 VD: 
- Nombre d'épisodes anxieux la semaine dernière
- score sur échelle d'anxiété
- indice de bien-être subjectif











