![[metrie - Chapitre 6.pdf#height=500]]

# Modèle de Rash
Comment comparer 2 items provenant de 2 tests différents? La comparaison ne peut faire sens que si les 2 tests ont exactement la même difficulté et discrimination. Or c'est très difficile. 

Le modèle de Rash ne nécessite pas de comparer précisément les différents items. On pourra ramener tous les individus sur un seul et même continuum tant que les items ont un lien entre eux. 
=> On pourra donc comparer les individus entre eux étant donné qu'ils seront ramenés sur un même continuum. 

Pour un individu donné, je pourrai calculer la probabilité de réussite d'un item en fonction de la difficulté de l'item. 


Compétence d'un sauteur?
 - recondrd individuel?
 - score à un tournoi?
on ne sait pas comment la mesurer ainsi, il faut donc un test standardisé. Plus on augmente la difficulté, plus on commence à voir des échecs; il faut donc trouver une portée de questions qui mettent les gens en difficulté. On a des questions qui sont systématiquement réussies puis des questions qui sont systématiquement ratées puis tout ce qui se trouve au milieu.

Compétence = difficulté de l'item pour laquelle la probabilité de réussite est de 0.50. Ce pour quoi le sujet sait répondre est à 0.50. Pour ce qui sera plus difficile ou plus simple, la probabilité s'éloignera de 0.50 et ne reflétera plus la compétence de l'individu. 

![[Pasted image 20260401114419.png|inlL|400]]bleu aura de meilleures perfs que rouge mais on sait les représenter tous les deux. leu aura de meilleures perfs que rouge mais on sait les représenter tous les deux. leu aura de meilleures perfs que rouge mais on sait les représenter tous les deux. leu aura de meilleures perfs que rouge mais on sait les représenter tous les deux. 




Si la compétence d'un sujet est inférieure à la difficulté de l'item d'une unité: la probabilité de répondre correctement à la question sera de 0.27.
Si la compétence d'un sujet est supérieure à la difficulté de l'item d'une unité: la probabilité de répondre correctement à la question sera de 0.83.
Si la compétence d'un sujet est inférieure à la difficulté de l'item de deux unités: la probabilité de répondre correctement à la question sera de 0.12.
Si la compétence d'un sujet est supérieure à la difficulté de l'item de deux unités: la probabilité de répondre correctement à la question sera de 0.88.



On veut centrer la moyenne des scores sur 0.
On peut comparer des questions de difficulté similaires. 

Si on veut pouvoir comparer les scores entre individus, il faut s'assurer que les individus aient répondu à toutes les questions. Pourtant PISA adapte la difficulté des questions et les questions posées ne sont pas les mêmes pour chaque étudiant. 

Calculer la compétence pour un pattern (1, 1, 0, 0)

|        |        | Reussi | B=-1 <br>(si la compétence de la personne était de -1) | B=0  | B=1  |
| ------ | ------ | ------ | ------------------------------------------------------ | ---- | ---- |
| Item 1 | D=-1   | 1      | 0.5                                                    | 0.73 | 0.88 |
| Item 2 | D=-0.5 | 1      | 0.38                                                   | 0.62 | 0.82 |
| Item 3 | D=0.5  | 0      | 0.82                                                   | 0.62 | 0.38 |
| Item 4 | D=1    | 0      | 0.88                                                   | 0.73 | 0.50 |
|        |        |        | 0.14                                                   | 0.21 | 0.14 |
On postule l'independance totale entre les 4 items. La probabilité d'observer le pattern 1,1,0,0 est de:
P(Item_1 = 1) * P(Item_2 = 1) * P(Item_3 = 1) * P(Item_4 = 1) = probabilité d'observer une réponse correcte à l'item 1 * la probabilité d'observer une réponse correcte à l'item 2 * ...

**Indépendance totale** : on suppose qu'il n'existe pas de lien entre le genre et la couleur des yeux. La probabilité d'observer un homme aux yeux bruns = probabilité d'observer un homme * probabilité d'observer une personne avec des yeux bruns. 
=> Possible seulement quand les deux variables sont indépendantes. 

Observation 1: Pour ces questions reprises dans le tableau, dont la difficulté est croissante, la probabilité d'occurrence de patterns sera plus grande pour (1,0,0,0) que pour (0,0,0,1).
![[Pasted image 20260408111433.png|500]]
De même, pour un score de 2, les pattern les plus probables sont (1,1,0,0) et (1,0,1,0) et le moins probable est (0,1,1,1). 


# Données manquantes
**Calculer la somme** est une mauvaise idée. 

**Calculer la moyenne:** Certains diraient de calculer la moyenne sur le nombre d'items répondus (4/5 donc je fais la somme de 4 items/4). Ne tient pas compte des différences de difficulté des questions et des questions ignorées. Reste mieux que de calculer la somme, pour autant que la difficulté ne varie pas fortement. 

**Remplacer toutes les données manquantes par la moyenne de la variable**. Si un individu n'a pas répondu à la Q5, on calcule la moyenne de toutes les réponses à la Q5 et on remplace le résultat par cette moyenne (obtenus par les autres participants). On considère que l'individu est un individu moyen. On surestime les individus faibles et on sous-estime les individus compétents. 



**Ramener deux tests sur un même continuum**
Si certains items sont partagés entre 2 tests, on pourra trouver la difficulté de ces questions pour les deux groupes (Ex: Groupe 1: D=-1, Groupe 2: D=0).  
![[Pasted image 20260408114234.png|500]]

