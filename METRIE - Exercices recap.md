**KR20**
Si le questionnaire est composé uniquement d'items dichotomiques, le KR20 ou l'alpha de Cronbach donneront le même résultat.

$\rho_{tt} = kr20 = \dfrac{k}{k-1} \dfrac{\sigma^2_t - \sum^k_{i=1}p_iq_i}{\sigma^2_t}$

$k$ = nombre d'items
$p_i$ = probabilité de réussite à l'item
$q_i$ = probabilité d'échec à l'item
$p_i$: compter le nombre de sujets ayant répondu correctement / nombre total de sujets. Exemple: 9/20

qi: on compte le nombre de sujets ayant répondu incorrectement / nombre total de sujets (raccourcis: ou alors on fait $1-p_i$)
La somme de q_i et p_i doit faire 1.

Ensuite, on multiplie les $p_i*q_i$ dans une colonne dédiée puis on pourra appliquer la formule. 

**Alpha de Cronbach**
On peut utiliser le même résultat que celui du KR20 - il ne donne pas d'exemple complet de l'alpha de Cronbach ici

**Kuder-Richardson**
p_m = probabilité moyenne de réussite (somme des probabilités de réussite / k) (ex: 0,51)
q_m = probabilité moyenne d'échec (somme des probabilités d'échec / k) (ex: 0,49)

**Erreur standard de mesure $(\sigma_e)$**
On veut calucler l'interval de confiance autour du score total d'un sujet. Nous donnera le degré de précision de l'uinstrument de mesure et de confiance en les valeurs obtenues.

Score total: 2,62 
Valeur obtenue par le KR20: 0,71
$\sigma_e = \sigma_t\sqrt{1-\rho_{tt}} = 2,62\sqrt{1-0,71}$
Pour le score de l'individu 13, qui a eu un score total de 7, l'interval est de 7 +- 1,96 * 1,41 = [4,24 : 9,76]
1,96 est la valeur critique pour un Z latéral, (correspondant à 95% de certitude?)


**Analyse d'items**
Propriétés psychométriques des items:
- discrimination

**Score de discrimination**
corrélation bisériale de points pour l'item 4
$M_r$= moyenne des scores totaux des sujets ayant réussi à l'item / nombre de personnes ayant réussi.
$M_e$= moyenne des scores totaux des sujets ayant échoué à l'item / nombre de personnes ayant échoué.

$r_{pbis} = \dfrac{M_r-M_e}{\sigma_t}\sqrt{p_i*p_i} = \dfrac{6,69 - 2,14}{2,62}\sqrt{0,65 * 0,35} = 0,83$ Proche de 1, donc on considère que cet item mesure bien le construit.

Pour l'item 3, la moitié qui ont bien répondu, l'autre moitié qui ont mal répondu
$M_e = 5,2$
$M_r = 5$
$r_{pbis} = -0,04$
$p_i$ et $q_i$ dont les même que ldans les exercices précédents


**Fidélité sans l'item 3 (alpha de Cronbach)**
Je prends l'alpha de Cronbach de 0,71 et j'utilise un n de -1 (demandé dans l'énoncé, on retire un item et on veut la nouvelle corrélation). 
Supprimer un item peut augmenter la corrélation lorsque cet item ne corrèle pas du tout avec le score total. 

**Indice de difficulté de l'item**
$p_i$: indice de difficulté
7/20 = réussite /nombre de questions totales

Indice de difficulté corrigé pour choix au hasard (avec 4 solutions proposées)
$p_e$ = probabilité d'échec

$p_e = p_r - \dfrac{p_e}{k-1} = 0,35 - \dfrac{0,65}{4-1} = 0,13$

**Fidélité d'une batterie composée de k sous-tests**
La matrice de variance-covariance de trois sous-tests (dénommés A, B, C) est présentée ci-dessous. La variance totale du test est égale à 36,59.
=> On aurait pu ne pas nous donner la covariance car on pourrait devoir la calculer nous-même.


|             | Sous test A | Sous test B | Sous test C |
| ----------- | ----------- | ----------- | ----------- |
| Sous test A | 8,14        |             |             |
| Sous test B | 3,28        | 2,65        |             |
| Sous test C | 4,43        | 1,61        | 7,16        |

$\alpha = \dfrac{}$ // à compléter

