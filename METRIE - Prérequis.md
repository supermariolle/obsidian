![[Prerequis.pdf]]


La taille (VI) est la variable latente et j'utilise le score sur cette variable pour prédire si une personne sera capable de toucher le diffuseur (baffle placé plutôt haut). Si la personne fait 1.4m, la probabilité qu'elle le touche est faible. 

La variable latente (taille) constitue la variable indépendante. La variable observée (probabilité que la personne touche le baffle) sera la VD, car elle dépend de la taille.

Dans toute prédiction, il y a un *résidu*, càd une proportion que je n'arrive pas à expliquer. Différence entre ce que j'observe et ce qui est prédit. 

L difficulté d'un item correspond au niveau de compténeces nécessaire pour avoir un niveau de réussite de 0.50.
Au dessus de 0.50, la probabilité de réussite est supérieure à la probabilité d'échec. 

.50 est le point d'inflexion.
Si on regrade la courbe jaune, jusqu'à .50, la pente ne fait que devenir de plus en plus à la verticale. A partir de .50, la pente commence à diminuer. 0.50 est le point d'inflexion. 

Dans un test à questions oui/non, j'ai besoin de connaitre 
- la compétence du sujet
- La difficulté de l'item (conditionné par: hauteur de l'objet, est-ce qu'il joue au basket, etc).

-5: individus les plus petits
+5: individus les plus grands
item facile: facilité calculée sur base du nombre de réponses correctes. 

Si la réponse de l'élève représente un individu de grande taille je mets 1.
Si la réponse de l'élève représente un individu de petite taille je mets 0.

"J'ai besoin de quelqu'un de grand pour m'aider à attraper un objet en hauteur": oui (donc il est petit, je lui mets un 0 pour cet item).

Je vois que pour la question numéro, 5, j'ai la plus grande proportion de trouver des 1 (tout le monde se considère comme suffisamment grand pour répondre par "non, cette difficulté liée à ma taille n'est jamais/pas souvent arrivée").
"Dans les toilettes publiques, il arrive souvent que les miroirs soient placés trop haut."

La question numéro 4, la plus difficile (tend à avoir beaucoup de 0). Si je ne prends pas une grande taille pour mes chemises, les manches sont trop courtes. 

**==Courbe discontinue vs courbe théorique==**
La courbe discontinue doit se rapprocher le plus e la courbe théorique. On veut que les données se rapprochent du modèle. Si la courbe discontinue n'est pas proche de la courbe théorique, on peut supposer que l'item n'apporte pas grand chose par rapport à ce que je veux mesurer. 
"On m'a déjà dit: tout ce qui est petit est joli". Correspond plutôt bien à la courbe théorique.
"Pas question de finir un repas sans un dessert": La courbe discontinue est fort éloignée de la courbe théorique: peu pertinente pour ma mesure. => quel que soit votre poids, la probabilité de répondre OUI est pratiquement identique. Elle ne varie donc pas selon la différence de poids et ne contribue pas à la mesure précise du poids d'une personne. 
Q: comment est créée la courbe théorique, sur base de quoi? 
**La courbe théorique** indique quelle est la probabilité qu'un individu réussisse un item sur base de la compétence de l'individu. 
**La courbe empirique** indique quelles sont les réponses effectivement apportées par les participants.

**==Difficulté d'un item==**
Certains items n'apporteront aucune information. Placer une barre à 5cm pour tester le saut en hauteur n'apportera rien, de même que la placer à 3m. 
Si les individus apportent tous la même réponse, on n'obtiendra aucune information.
Les meilleures questions sont celles auxquelles les probabilités de réponses sont de 0.5. 

Quand on se contente, dans l'estimation des compétences, de calculer un score qui correspond au nombre de réponses correctes, passer de 1 à 2, n'a pas nécessairement la même implication qu de passer de 5 à 6.
1: 5+5
2: 10+10
5: 234 + 543
6: Calcule la dérivée de blabla (saut en compétence bien plus important). 

Si on prend en compte la difficulté des questions, ça signifie qu'on n'a plus besoin de poser les mêmes questions à tout le monde pour ramener les résultats sur la même échelle et réaliser des comparaisons. 
Un intérêt majeur de la théorie des modèles de score à l'item, en prenant en compte la difficulté, je ne suis plus obligé de poser les mêmes questions aux individus (pas compris). 

**==Analyses factorielles confirmatoires==**
On veut construire une variable latente dans le but de prédire ce qu'on va observer dans les questions. 
Pour prédire ce que j'attends de l'item A1, je multiplie un coefficient (un simple facteur entre -1 et 1) par la variable latente (taille de l'individu).


Si il y a correlation entre les résidus, ça signifie clairement qu'il existe une 


**==Méthodologie==**
**Étape 1**
on decide ce qu'on va mesurer (taille, intelligence etc)
**Étape 2** 
Collecte - no va créer des questions, on choisit les sujets, les lieux de passation de test (on veut un lieu silencieux). 
**Étape 3**
Transformation d'observations en données. J'observe les réponses données par la personne (observation) en données (1 ou 0 si la réponse est correcte/fausse). 
**Étape 4**
Application d'un modèle de mesure sur ces données. 

Traitement statistique
**avec une seule échelle ordinale**
Echelles absolues et relatives (nombre d'indivisudus ou % d'individus plus petit ou égal à une catégorie donnée)

Avec deux échelles ordinales (les mêmes individus sont classés selon 2 critères distincts). 
F. Cum. Abs: fréquences cumulées absolues
F. Cum. Abs: pourcentage de participants de la catégorie



**Échelles d'intervalles égaux** (exemple: la température en C°)
Échelle ordinale avec signification des distances
Quand il fait 20°C, il ne fait pas 2x plus chaud que quand il fait 10°C. 

**Échelles de rapport**
Même chose que pour les échelles d'intervalles égaux mais avec un 0 qui vaut un 0 absolu.
Sur une table j'ai 2 pommes, sur l'autre j'en ai 1. Il y a bien 2x plus de pommes sur la première table. Le rapport entre les valeurs est pertinent. 

# Les distributions théoriques
## La distribution normale
$-\infty+\infty$
Variable continue (infinité de valeurs possibles)
Symétrique
$f(x) = $

Limite centrale: si je prends un certain nombre de variables (taille, QI, poids, etc), quelle que soit la distribution, pour autant que les variables soient indépendantes (les phénomènes ne corrèlent pas).
le poids et la taille ne sont pas indépendants (il ya  corrélation).
Si les phénomènes sont indépendants et que je calcule la somme de ces distributions, j'obtiens une distribution normale. 

La fonction de densité donne la hauteur de la barre rouge 

Si j'ai une fonction T de student avec un dl de 35, la distribution est tellement proche de la distribution normale qu'on peut commencer à appliquer les théories de la distribution normale. 

