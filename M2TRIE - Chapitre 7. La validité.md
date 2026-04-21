
# Rappels
----

Fidélité = pourcentage de vrai dans mes mesures. Var scores vrais / var scores totaux. 
1) Test-restest (stabilité des scores à travers le temps, ex anxiété d'une personne est-elle un trait stable ou peut-elle varier selon les situations. Par contre, l'empathie est + stable que l'anxiété). 
2) Méthode de consistence interne. Le test est-il unidimensionnel?
3) Méthodes mixtes. On rencontre cette méthode très rarement dans la littérature donc on ne s'attarde pas dessus.
Dans le cadre des sciences humaines, il est impossible de déterminer le score vrai car on ne sait pas mesurer parfaitement .
Score observé = Score vrai + score d'erreur


# Validité
---
Rien à voir avec la stabilité temporelle ou la consistence d'une mesure

**==Validité==**: capacité d'un instrument de mesure de mesurer ce qu'il prétend étudier.

2 idées majeures:
- **le test mesure réellement ce qu'il prétend mesurer**
  
- **Quels traits sont mesurés par le test?** à quoi va servir cette mesure? Permet-elle de prédire des éléments intéressants? Si je veux prédire les compétences sportives d'un footballeur, un test d'intelligence ne permettra pas de prédire les capacités au football. Par contre, mesurer sa condition physique va corréler avec les compétences sportives footballistiques. 

La validité peut-être représentée sous forme de corrélation.
Dans la fidélité, la variance obs est composée de 2 choses:
- La variance vraie
- La variance d'erreur

Pour la validité, on calcule une corrélation entre le score à un test de QI et un score qui pourrait représenter la réussite professionnelle d'un individu.
Un phénomène aléatoire ne peut pas corréler avec autre chose. Quand je veux calculer la corrélation entre le QI et la réussite professionnelle, une corrélation parfaite serait tout de même atténuée par les erreurs. 

Ex: corrélation entre QI (X) et réussite professionnelle (Y)
=> Quelle que soit la mesure, elle sera entachée d'une erreur.
QI = X + E1
Réussite professionnelle = Y + E2 (score obtenu au test de réussite professionnelle, incluant les erreurs)

Corrélation = covariance / sqrt(écarts-types)

cov(X + E1, Y+E2) = cov(X,Y) + cov(X, E2) + cov(E1, Y) + cov(E1, E2)
Avec les postulats indiquant que les correlations des erreurs est de 0, on peut donc retirer tout ce qui inclut

$P(X, E1, Y+E2) = \dfrac{cov(X, Y)}{\sqrt{(\sigma^2_{(X)}+\sigma^2_{(E1)})*(\sigma^2_{(Y)}+\sigma^2_{(E2)})}}$
Plus les erreurs de mesures sont importantes, plus on sous-estimera la corrélation. Si les mesures étaient parfaites, on aurait une corrélation (par exemple) de 0.8. Mais avec les erreurs de mesures, on augmentera le dénominateur (inclut les variances des erreurs) et ça diminuera donc la corrélation calculée

**Il existe donc une correction de la corrélation.**
$P(\infty, \infty)$
Fidélité de 0.9 pour X et Y? 0,9/sqrt(0,90 * 0,90) = 1
$\rho_{(\infty, \infty)} = \dfrac{\rho(X, Y)}{\sqrt{\rho(X, X)* \rho(Y, Y)}}$


# La validité prédictive
Je créé un test d'intelligence: valider un nouveau test par un ancien test qui mesure/prétend mesurer la même chose. Par contre, pour la validité prédictive, on utilise un critère externe (mesure du QI). 
Pour que mes mesures soient correctes, elles doivent -répondre à certaines conditions:
- **pertinentes** (revenus salariaux <> réussite professionnelle)
- **fidèle** au sens défini dans le chapitre 5
- la mesure du critère extenre ne peut pas être **contaminé**. Ex: je veux développer un instrumer pour mesurer le burnout. Je valide cette mesure du burnout en demandant à un psy une évaluation clinique des participants. De plus, j'informe le psychiatre des résultats de mon test. Si le psychiatre se rend compte que nous avions surestimé donc il pense devoir adapter ses propres évaluations ("j'ai du être trop exigeant, vu les points qu'on lui a donné")
- **auto-corrélation**: une composante du critère externe ressemble fortement à une des mesures de mon test


## 3 méthodes pour déterminer la validité prédictive

==**Le coefficient de corrélation**==
- Bravais-Pearson
- Corrélation bisériale de point

==**L'indice d'efficacité**==
Définition d'un seuil, par exmeple un examen d'entrée.
Dans quelle mesure cet examen permet-il de prédire la réussite des individus? 
Critère externe = l'individu réussit sont BAC 1 OU l'individu réussit son BAC et 5 ans
Accepté/refusé à l'examen - résultat dichotomique


|                 |                             | Echec du BAC 1   | Réussite         |
| --------------- | --------------------------- | ---------------- | ---------------- |
| Test prédicteur | Accepté à l'examen d'entrée | A inexact (+, -) | B exact (+, +)   |
|                 | Refusé à l'examen d'entrée  | C exact (-, -)   | D inexact (-, +) |
C et B sont les résultats cohérents. A et D ne le sont pas. 

==La validité de contenu==
- **La validité apparente**: je demande à un expert reconnu de déterminer si ce que je mesure est correct. Jugement d'expert
- **La validité logique**: validité d'échantillonnage. mon test mesure la compréhension de l'écrit et donc je prends en considération les aspects de la compréhension (textes littéraires, compréhension de graphiques, tableaux etc). Dans le processus de la lecture on a 1) retrouver des infos, 2) interpréter les infos, 3) évaluer les infos. On peut donc créer une table de spécifications dans laquelle on va insérer les résultats obtenus.

==La validité théorique==
Pas de critère externe
Pas d'unive

- **La validité convergente** (validité intra-concepts): détermine dans quelle mesure les résultats observés dépendent des choix méthodologiques que j'ai adoptés. On veut que ce ne soit pas déterminé par les choix méthodologiques. Avec une validité convergente, un test de psychologue ou un test papier auraient quasiment les mêmes résultats. 
- **La validité divergente**: détermine si les résultats de ma mesure corrèlent avec des mesures déjà existantes - mon test est-il différent des tests déjà existants? Sinon, je ne mesure pas un nouveau concept. 

Imaginons qu'on veuille mesurer:
- estime de soi (A)
- sociabilité (B)
- contrôle de soi (C)
3 méthodes de mesure:
- test papier (1)
- retour enseignant (2)
- retour parents (3)

VOIR DIA avec tableau
=> 3 méthodes, 3 mesures, Chaque individu aura 9 scores (A1, A2, A3, B1, B2, ....)
Les cellules rouges dans une matrice de corrélation (A1/A1) contiendront la fidélité de la mesure avec elle-même. On veut tendre vers 1 pour avoir une fidélité élevée. 
**Les cellules vertes** indiquent les liens des différents concepts au sein d'une méthode (corrélation estime de soi/fidélité pour la méthode papier-crayon). 
Les cellules bleues sont les corrélations pour un concept donné à travers différentes méthodes (validité convergente). On veut que la corrélation entre 2 mesures différentes (2 instruments de mesure) pour un même concept tende vers 1. Sinon, l'instrument de mesure entache ma mesure. 
**Les cellules blanches** corrélations entre différents concepts et différents méthodologies. On veut que les corrélations soient les plus faibles possibles

==**L'indice de séparation des groupes**==
- test $t$ (on veut prédire une var continue, la variable indépendante est nominale: analyse de la variance à 2 modalités donc test $t$). 
	- La différence est-elle significative?
	- dépend de la taille d'échantillon
	- taille de l'effet (différence/écart-type)


