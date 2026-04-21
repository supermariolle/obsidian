
Mesures de corrélation: les valeurs peuvent être ordonnées. "Est-ce que si je connais les résultats de l'un, je peux dire quelque chose des résultats de l'autre?"

Mesure d'association: les valeurs ne peuvent pas êtres ordonnées. "Est-ce que les hommes réussissent mieux que les femmes?"


Corrélation - RAPPEL
1. Corrélation bisérielle de point
2. Corrélation de Spearman (non paramétrique quand on a des problèmes de normalité)
3. Coefficient de concordance de Kendall
4. Corrélation partielle (??on ajoute une VI supplémentaire dans l'ensemble de la corrélation?? pas compris)


# Pearson 
**==coefficient de corrélation de base, le plus classique==**
Relation entre 2 variables continues X et Y \[-1;1]

$$r=\frac{cov_{XY}}{S_XS_Y}$$

La covariance est basée sur les unités choisies. Il faut donc le standardiser sur une échelle qui va de -1 à +1. 


# Corrélation bisérielle de point
Corrélation avec variables dichotomiques. Les variables (voire les 2) sont nominales à condition qu'il n'y ait que 2 valeurs possibles (ex: réussi, échoué, masculin/féminin).

On peut remplacer une valeur par un chiffre: Masculin (8) et Femme (18). Quelle que soit la valeur qu'on va choisir, la corrélation donnera le même résultat 👏
Conseil: plus facile avec 0 et 1. 

Droite de régression:
a = moyenne du groupe auquel on a attribué 0 = 74,43
b (pente): pour passer de 0 (moyenne des hommes) à 1 (moyenne des femmes) = -66,44 - 74,43 = 7,99






# **Deux variables dichotomiques**
Réussite/échec & Masculin/féminin. On va transformer en 0 et 1 pour pouvoir calculer une corrélation. 

Relation entre genre et réussite en B1?
X = genre
Y = résultat
N=18


| Sujet | Genre (X) | Résultat (Y) | X^2 | Y^2 | XY  |
| ----- | --------- | ------------ | --- | --- | --- |
| 1     | 0         | 0            | 0   | 0   | 0   |
| 2     | 0         | 1            | 0   | 1   | 0   |
| etc   |           |              |     |     |     |
X^2 et Y^2 pour calculer l'écart-type. Mais on n'a pas besoin de les calculer car pour 0 et 1, les mettre au carré garde la même valeur. 
Pour XY, c'est toujours 0 sauf si X et Y valent 1 (raccourcis).

S_x(écart type pour X)
S_y (écart type pour Y)
r_{pb} = cov_xy / SxSy = 0,555/(0,511x0,514) = 0.209 (coefficient de corrélation)
r_{pb}^2 = 0,209^2 =0,04 => "4% de la variabilité touchant la réussite peut s'expliquer par le genre." 


$\chi^2 = N * \phi^2$
Si j'ai phi, je peux trouver le chi^2 => le test d'hypothèse passe par l'obtention du chi^2 car on aura phi.
$\chi^2 = N * \phi^2 = 18 * 0,209^2 = 0,79$
$\chi^2_{0,05}(1)=3,84$$\$

Puisque 0,79 < 3,84 ne pas rejeter $H_0$



# Corrélation pour données rangées
Coefficient de corrélation quand on a un problème de normalité avec les données.
Transformation de données en rangs. 
- Cas 1: Données déjà sous forme de rangs = classement (si n a des participants qui font une course et on a le classement - 1er, 2eme, 3eme, etc). Les données sont déjà rangées
- Cas 2: 

**==Coefficient de Spearman**==
Calcul de corrélation sur des données transformées en rangs. Appliquer la formule habituelle sur les rangs. 

$r_S= 1 - \dfrac{6\sum D^2}{N*(N^2-1)}$

Relation entre les résultats de math et bio?
N=10


| Math | Rangs X | Biologie | Rangs Y | X^2 | Y^2 | XY  |
| ---- | ------- | -------- | ------- | --- | --- | --- |
| 57   | 3       | 83       | 7       | 9   | 49  | 21  |
| 45   | 1       | 37       | 1       | 1   | 1   | 1   |
| 72   | 7       | 41       | 2       | 49  | 4   | 14  |
| etc  |         |          |         |     |     |     |
| 682  | 55      | 679      | 55      | 385 | 385 | 349 |

Quand on n'a aucun ex aequo dans les données, la somme des Y et Y doivent être les mêmes (car on a 1, 2, 3, 4, 5, ..., 10 dans les 2 colonnes). Ici: 55.
De même, les mettre au carré doivent aussi ramener le même résultat => $X^2 = Y^2$

Une fois que j'ai ça, je fais la formule habituelle de la covariance: 
$Cov_{xy}$ = 5.17

Idem ici: la variabilité pour X et Y sont les mêmes car les rangs sont les mêmes entre X et Y (1,2,3,4)
$S_X = 3,03$
Donc $S_Y=3,03$ également

$r_X = \dfrac{Cov xy}{S_xS_y} = 5,15 / (3,03*3,03) = 0,56$

**==2ème formule:==** 
Ne s'applique que quand on n'a pas d'ex-aequos. 
Calcul des rangs aussi:


Différence à faire dans le sens qu'on veut

| Rangs Math | Rangs Bio | D   | D^2 |
| ---------- | --------- | --- | --- |
| 3          | 7         | -4  | 16  |
| 1          | 1         | 0   | 0   |
| etc        |           |     |     |
|            |           |     | 72  |
$r_S = 1 - \dfrac{6\sum D^2}{N*(N^2-1)}$
$r_s = 1-\dfrac{6*72}{10*(100-1)} = 0,56$

Corrélation? Test d'hypothèse.
$H_0: \rho_s = 0$ => pas de lien entre les deux variables
$H_A: \rho_s \neq 0$ => corrélation entre les deux variables

Table de valeurs critiques sous forme de corrélations => 
(test bilatéral)
$r_S = 0,56 < r_{s0,025} = 0,648$ 
La valeur de la corrélation doit être plus grande que la valeur critique => ne pas rejeter $H_0$
0,56 semble être une corrélation importante mais on n'a que 10 sujets donc pas concluant. 

==**Coefficient (T) de Kendall==**
On ne la voit pas car c'est quasi pareil que Spearman