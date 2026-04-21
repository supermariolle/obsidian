![[Anova mixtes.pdf]]

Mélange de variables indépendantes inter et intra-sujets.

Exemple: 4 variables inter-sujets, 4 intra-sujets => plan mixte, 7 variables indépendantes.

Version la plus simple: 1 facteur inter et un facteur intra (2 VI) pour constituer un plan mixte.

Dans l'ANOVA factorielle, on avait les variables $a$ et $b$ (intervertibles comme on veut).

$\triangle\hspace{-0.54em}\small{!}$  Dans ce chapitre: 
$a$ = inter-sujets
$b$ = intra-sujets

Rappel: CM = SC / dl
Exemple: SC: 1378,54, dl: 1, CM: 137,85


# Exemple d'utilisation
On suit l'évolution des compétences d'élèves en mathématiques entre juin et septembre.
On va comparer 2 manières d'enseignement
- manière traditionnelle
- nouvelle méthode
On ne peut pas utiliser les mesures répétées, en enseignant d'abord avec la M1 puis avec la M2 (contamination évidente). Par contre, l'évolution à travers les mois est intéressante - quelle méthode offre la progression la plus rapide?

VD: nb de réponses correctes à 50 problèmes proposés
VI: M1, M2

Il y a un effet principal du mois (on voit une amélioration à travers les mois, et ce, pour les 2 méthodes).
Y  a-til une interaction entre les 2 méthodes? Oui car si on traçait une ligne pour les scores bleus et une pour les scores bleus hachurés, les lignes se croiseraient. 

Variabilité intra-sujets: Les scores d'un même sujet varient
Variabilité inter-sujets: variabilité des scores entre les participants. 
- erreurs liées à la variabilité du facteur A
- variabilité intra-groupe = variabilité inter-sujets

Variabilité totale = variabilité intra + variabilité inter
Variabilité intra = B, AxB, v. résiduelle

**==Variabilité totale==:** variance calculée sur l'ensemble de toutes les données 
N = Nombre de mesures totales de l'étude 

CM intra groupe = variance entre les scores d'un même groupe
CM_A = variance attribuée à la méthode d'enseignement
Le CM sujet: variabilité entre les moyennes de chaque participants. 
CM_intra-groupe
![[Pasted image 20260326150652.png]]


La variabilité intra-sujets:
Variabilité totale - Variabilité inter-sujets
$SC_{intra-sujets} = SC_{total}- SC_{inter-sujets}$


$CM_{AB}$ = interaction AxB
1) CM_{cellules} voir formule
2) $CM_{AB} = \frac{SC_cellules - SC_A - SC_B}{(dl_{cellules} - dl_A - dl_B)}$

Le carré moyen erreur est propre à chacune des deux parties: inter et intra - ne pas utiliser le CM_erreur $a$ pour calculer CM $b$


**==Si aucun résultat (moyenne) n'est fournie: utiliser la procédure de calcul rapide==**


Effet simple: regarder si une VD a un effet sur la VI sur une seule condition de la VI (technique nouvelle d'enseignement vs ancienne). 
Exemple: "Je teste l'effet de la méthode nouvelle sur 4 mois" - n'implique pas la méthode ancienne.
"Y a t-il un effet de la méthode en mars entre les deux méthodes?" - comparaison multiple


Effets simples: Tester l'effet simple du moment avec la méthode classique vs la méthode nouvelle. On compare une méthode avec elle-même dans le temps, pas entre elles (nouvelle/ancienne). Anova chapitre 6, mesure répétée

H0: il n'y a pas d'effet du moment sur la méthode nouvelle
HA: il y a un effet du moment sur la méthode nouvelle


Exemples de comparaisons multiples:
- "différences de moyennes au mois de juin entre les deux méthodes?"
  C'est un effet simple aussi donc soit on calcule l'effet simple, soit on fait une comparaison multiple (test de Dun-Bonferroni est un peu plus rapide que l'effet simple)
- Comparer septembre et juin pour la méthode nouvelle. Effet simple aussi mais intra-sujets car on compare les mêmes élèves
- Compare méthode classique en septembre avec méthode nouvelle en juin (comparaison en diagonale - peu utilisé/pertinent)

CM combiné étant une espèce de moyenne entre le CM_intragroupe et le CM_résiduel, il se trouvera toujours entre les 2 valeurs:
Ex: 
CM_intra:  137,85
CM_résidule: 29,38
CM_combiné: 56,85 =>> OK car entre les 2 précédents


**Conditions d'application pour les plans mixtes** (pas de problèmes à l'examen sauf pour la sphéricité)

**Normalité**

**Homogénéité des variances pour les facteurs inter-sujets**

**Sphéricité**: uniquement pour les différences intra-sujets. Alt: Manova ou ajuster (diminuer) les degrés de liberté pour obtenir une valeur critique plus sévère = multiplier les dl par un facteur correctif (epsilon: $\epsilon$):
Si on nous donne epsilon
dl B = (b-1)*$\epsilon$
dl AB = (a-1)(b-1)*$\epsilon$


Pas de respect des règles = pas de tests alternatifs. Solution, tenter de transformer les données (comment?) ou de faire des anovas séparément sur des sous-ensembles de données mais avec moins de possibilité de répondre à des questions larges. 





