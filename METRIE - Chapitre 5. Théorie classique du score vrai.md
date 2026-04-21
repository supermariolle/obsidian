![[metrie - Chapitre 5.pdf]]
Un non est toujours considéré comme une réponse incorrecte. 

Je peux calculer le nombre de réponses incorrectes par individu et le nombre de réponses correctes par question. 

|         | Q1  | Q2  | Q3  | ... | Total |
| ------- | --- | --- | --- | --- | ----- |
| Sujet 1 | 1   | 1   | 0   |     | 2     |
| Sujet 2 | 1   | 0   | 1   |     | 2     |
| Sujet 3 | 1   | 1   | 1   |     | 3     |
| ...     | 3   | 2   | 2   |     |       |

On a des outils statistiques qui permettent d'identifier quelles questions nous permettent de différencier les individus. (Exemple: du saut en hauteur: à 0,30cm, le saut ne différencie personne car tout le monde réussit).
=> **la meilleure question** est une question qui divise en 2 la population: 50% de réussite à la question: écart-type maximal. 
probabilité de réussite: 0,5
Si la corrélation était égale à 1: on sait que si la personne répond mal à la Q1, elle répondra mal à toutes les autres (car corrélation de 1 entre toutes les questions).
On aimerait donc obtenir une corrélation entre items soit la plus proche de 1, car ça permettrait de différencier les individus. 

> [!info] Corrélation élevée (max à 1) ET probabilité de réussite à 0.5 = max de différenciation entre les individus. 

Si mes items ne corrèlent pas, ça signifie que j'additionne des pommes et des poires, ce qui rend absurde et inutilisable le résultat. 

Variance d'un item dichotomique (formule à connaitre #tuyau)
n = 
p = proportion de réponses correctes
q = proportion de réponses incorrectes



# Théorie classique du score vrai
Le score que j'observe est composé de 2 éléments: le score vrai ET le score d'erreur.
Si j'arrive à estimer l'erreur, je peux tenter de mieux estimer le score vrai. 
Un instrument parfait (n'existe pas) nous donnerait le score vrai. 

$X_\infty$ = score vrai
$X_t$ = score observé
$X_e$ = score d'erreur

$X_t = X_\infty  + X_e$
=> score observée = score vrai + score erreur

Trois postulats:
- La moyenne des erreurs est égale à 0 - on suppose qu'il n'y a pas de biais systématique. 
  $µ_{(X_e)} = 0$
  => la moyenne des scores observées = la moyenne des scores vrais (si les erreurs sont en moyenne de 0)
  
- La corrélation (et la covariance) entre les scores vrai et le score d'erreur est égale à 0. Globalement, il n'y a pas de biais systématiques ni de biais pour des sous-groupes d'individus. 
  Si il existait une corrélation (ce qui n'est pas le cas), avoir un grand score entrainerait aussi une grande erreur, et inversement, un score faible entraine peu d'erreurs. 
  
- La corrélation (et la covariance) entre les erreurs est égale à 0.
  Le fait d'additionner des erreurs avec le théorème de limite centrale, on peut postuler que les erreurs se distribuent normalement. 

La fidélité:
Plus mes scores d'erreur varient peu, plus mon instrument de mesure sera fidèle. Si il varie beaucoup (grandes erreurs), alors mon instrument n'est pas très fidèle. 
Corrélation d'un test avec lui-même.
Proportion de vrai entre ce que j'observe. Proportion de variance des scores vrais par rapport à la variance du score total. 
$p_{tt}=1-\frac{\sigma_e^2}{\sigma_t^2}$ = rapport entre variance du score vrai et du score d'erreur. (t=total, e=erreur, $p_{tt}$=fidélité)
Précision avec laquelle un score représente l'aptitude d'un sujet observé. 
ESM (Erreur standard de mesure) = ecart-type des scores d'erreur. 
${ESM} = \dfrac{1}{\sqrt{\sum^{n=i}_i} p * q}$
$ESM = \sigma_e$


Plus les erreurs de mesure sont importantes, plus la distribution bleu (observés) va s'éloigner de la distribution des scores vrais. Pour une mesure précise, la distribution des observés doit s'approcher des scores vrais. Si ils sont près, les erreurs de mesure sont petites et la mesure sera de qualité. 

Pour calculer l'erreur standard de mesure:
$\mu_(QI) = 100$
ecart type 15
fidélité = 0,89
ESM = $\sigma_e = \sigma_t*\sqrt{1-p_{tt}} = 15*\sqrt{1-0,89} = 5$
In individu estimé à 105 aura un interval de confiance de 95 à 115 ?? Uh?

Si j'allonge mon test, je peux en améliorer la fidélité.
Si je double la longeur d'un test, on peut démontrer que 

$p_{nt}=\dfrac{3.(0,70)}{1+(3-1)*(0.70)}=\dfrac{2.1}{2.4}=0.875$

Test de 20 questions et une fidélité de 0,85, or il souhaite une fidélité de 0,90. La formule permet de déterminer le nombre de questions à ajouter à la mesure pour obtenir la fidélité souhaitée.

$n=\dfrac{p_{nt}(1-p_{tt})}{p_{tt}(1-p_{nt})} = \dfrac{0,90(1-0,85)}{0,85(1-0,90)}=\dfrac{0,135}{0,085}=1,588$

nombre de questions nécessaires: 1,588 * 20 = 32 questions.

**==test-retest==** = corrélation entre T1 et T2, un seul test administré à deux moments différents.
Variance vraie: stabilité des scores
Variance d'erreur: instabilité des scores

**==Méthode de Rulon==**
J'ai un test de 10 questions. Je les classe de la plus simple à la plus difficile (ou de moins d'adhésion à plus d'adhésion - peu d'accord, fort d'accord) puis je mets les score dans des colonnes pair/impair. 

Ensuite, on calcule des scores de différence entre pair et impair puis on fait la variance des scores de différence. 



Les QCM et l'aléatoire
Un QCM en vietnamien à 4 propositions par question va me donner une moyenne de 2.5 sur 10 alors que ma compétence est de 0. On surestime donc la compétence par un test dont la réponse peut se trouver au hasard. Je mesure autre chose que la compétence.
Le bruit réduit les propriétés psychométriques de mon instrument de mesure. Puis surtout, il y a une inéquité.
Violation du premier postulat de la théorie du score vrai
Violation du second postulat de la théorie du score vrai: si on ne sanctionne pas les réponses incorrectes, on a intérêt à choisir une solution, ce qui va mener à une surestimation. La surestimation sera maximale pour les individus incompétents car les personnes compétentes répondront grâce à leur compétence réelle et n'obtiendront 0.25 points par compétence et non par chance (manque d'équité). 

2 solutions par question: 50% de chance de trouver au hasard
3 solutions par question: 33% de chance de trouver au hasard
...

Correction for guessing
![[Pasted image 20260401110635.png]]

k= nombre de solutions proposées
n=nombre de questions auxquelles on répond au hasard
Si il répond au hasard, il a 1/k chances de trouver la bonne réponse et
k-1/k de ne pas trouver la bonne réponse
5 suggestions: 1/5 de trouver la bonne, 4/5 de choisir une mauvaise

**Probabilité pour toutes les questions** (n* ... les formules plus haut)
n*(1/k) : probabilité de trouver la bonne réponse à travers toutes les questions
n*((k-1)/k): probabilité de choisir une mauvaise réponse à travers toutes les questions


**==Fonctionnement différentiel des items==**
Apparenté à la notion d'invariance.

**Notion d'invariance**: un test mesure de manière équitable des individus qui se différencient par certaines caractéristiques qui n'ont rien à voir avec ce que je prétends mesurer. 
Exemple: perception de l'utilité du métier par les professeurs. On essaye de voir si l'utilité perçue du métier varie selon qu'on enseigne en primaire ou en secondaire. Or, une question mentionne le terme "enfant". Elles ont donc apporté des résultats différents selon que l'enseignant enseigne en primaire ou en secondaire (les profs de secondaire ne se sentaient pas concernés par la question). 

A compétence égale, 2 individus qui diffèrent par une caractéristique qui n'a rien à voir avec ce que je prétends mesurer, auront des scores différents malgré une compétence égale. Si on considère que ma "compétence" est ma taille en cm, 1 personne de 1m85 ne pourra pas atteindre le diffuseur en sautant, tandis qu'une autre de même taille et qui aura pratiqué le basket saura l'atteindre. 


