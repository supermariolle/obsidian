[[STAT2 - Exercices récap]]
[[STAT2 - Rappels]]
[[STAT2 - Puissance]]
[[STAT2 - Chapitre 2 - L'analyse de variance à un critère de classification]]
[[STAT2 - Chapitre 3 - Comparaisons multiples entre des moyennes de traitement]]
# Rappels
**Statistique descriptive**: décrit un ensemble de données (moyenne, variance, corrélation, régression)
**Statistique inférentielle:** permet de tirer des conclusions générales à partir d'un échantillon limité.
Il y a beaucoup plus de matière en psychologie inférentielle; la plupart des études en psychologie reposent dessus. 

Erreur de première espèce: faux positif
Erreur de seconde espèce: faux négatif

![[psychostat-puissance.pdf]]
La puissance:

On peut tenter de la deviner grâce à des scenarios qu'on inventerait. "Calculez la puissance si la moyenne des avocats est de ceci/celà". En général, on ne connait pas la moyenne des avocats mais on peut tenter de la supposer sur des études précédentes; une étude aurait montré un QI de 104 en moyenne chez les avocats donc on le suppose à 104 pour calculer la puissance.  

Calculer la puissance, c'est calculer la probabilité d'avoir X avocats dont la moyenne sera > 104,935 si les individus proviennent d'une population dont la moyenne est de 104. 

**Puissance** = probabilité de rejeter H0 quand H0 est faux. Probabilité de prouver que les avocats ont 104 de QI (hypothèse que l'on pose parce qu'on a vu des résultats dans ce sens dans d'autres études), soit 4 points de plus que la moyenne de la population. Probabilité évaluée à ~0.34.

La puissance dépend de l'effet réel dans la population; autrement dit, si l'effet est grand dans la population, il y a de grandes chances de trouver un effet dans un échantillon également. 

Hypothèse du QI des avocats à 101 avec 25 avocats: puissance 0,0951 (9,5/100)
Hypothèse du QI des avocats à 110: puissance 0,9545 (95/100)
Plus l'effet est grand, plus avec la même étude

==**$+$ variance = $-$ puissance** ==
Plus la variance est forte, plus il sera difficile d'avoir une puissance importante. La variabilité impacte la puissance directement. 
Si on met en place des façons de réduire la variabilité, certaines adaptations réduisent la généralisation des résultats. On voudrait réduire la variabilité en regroupant des gens d'un âge plus similaire, donc on exclu des gens représentant des âges différents. 

On peut faire des tests bilatéraux: 96 - 104.

$H_A: µ > 100$   -> puissance si `µ = 96: 0`, si `µ=104: 0,3783`
$H_A: µ < 100$-> puissance si `µ = 96: 0,3783`, si `µ=104: 0`
$H_0: µ \neq 100$ -> puissance si `µ = 96: 0,2643`, si `µ=104: 0,2643`


*==Rappel==* :Quand on ne rejette pas l'hypothèse nulle, on ne rejette pas l'absence d'effet, on dit plutôt qu'on n'a pas suffisamment de preuve pour affirmer qu'il y a un effet. 

**La statistique $d$ de Cohen**
le $d$ de Cohen est une mesure de taille de l'effet. 
Il peut être appliqué pour presque tous les tests qu'on a vu. 

| Taille de l'effet | d    | Définition                            |
| ----------------- | ---- | ------------------------------------- |
| Petite            | 0,20 | Effet réel mais difficile à perçevoir |
| Moyenne           | 0,50 | Effet visible par un observateur      |
| Grande            | 0,80 | Effet facilement détectable           |

Chez les médecins, 5000 médecines sondés pour un QI moyen de 100,5
$d= \dfrac{X-µ}{\sigma} = \dfrac{100,5 - 100}{15} = 0,03$
d < 0,20 = effet très petit

Chez les notaires: la taille d'effet est soumise à l'erreur d'échantillonnage. 
=> "J'ai vu un effer de grande taille mais étant donné que le nombre de participants est très faible (on a que 5 notaires pour faire cette moyenne de 111, on ne conclura à rien".

$d= \dfrac{X-µ}{\sigma} = \dfrac{111 - 100}{15} = 0,73$
d+/- égal à 0,80, presque un grand effet. Or, la 

Si je n'ai pas l'écart type de la population, je dois utiliser un $d$ de Cohen appliqué à la formule du calcul de moyenne avec sigma inconnu
$d= \dfrac{X-µ}{S} = \dfrac{5,216-7}{1,832} = -0,97$



On doit calculer
1) Le d de Cohen
2) Le delta (voir dans le tableau des deltas , 1,30 => 0.37 pour un $\alpha$ de $0.5$)
   $\delta=d\sqrt{N} = $

**==Pour connaitre le nombre de participants requis selon la puissance souhaitée==**
Combien de sujets faut-il pour obtenir une puissance de 0.80 pour tester un QI de 104 dans un échantillon. 
On utilise la table de manière inverse; on reste dans 0.5, on cherche 0.80 et on voit que le delta correspondant est de 2,5.
$N = (\dfrac{\delta}{d})^2 = (\dfrac{2,5}{0,27})^2 = 85,7$
"*Est-il possible pour moi de trouver 86 avocats et de leur faire passer un test de QI?*"

**Estimer la puissance de l'étude avant de la réaliser nécessite**
a) Choisir le test statistique
b) Estimer la taille de l'effet réel
On estime à 104 le QI potentiel des avocats sur base d'études précédentes, évaluations personnelles)
c) Prévoir le nombre de sujets






