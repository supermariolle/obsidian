


**Général:**
- Ne pas répondre en pourcentage quand on demande la proportion
- "Peut-on affirmer que le traitement **modifie significativement**": ~~unilatéral~~ -> **bilatéral**


- $\sigma$: écart-type population
- $S$: écart-type de l'échantillon
- $\sigma^2$: variance population
- $S^2$: variance de l'échantillon
- $\mu$: moyenne population
- $\bar{X}$: moyenne échantillon
- $a$: ordonnée à l'origine sur la droite de régression
- $b$: pente de la droite de régression
- $\hat{Y}$: valeur prédite sur la droite de régression
$\,$
- **Non-rejet d'hypothèse nulle**: "On ne peut pas rejeter $H_0$. Dès lors, on n'a pas assez de preuves pour affirmer $H_A$"
- **Rejet d'hypothèse nulle**: "On peut rejet $H_0$. Dès lors on peut affirmer que $H_A$ est vraie."
- Test $t$: si $t_{obs}$ est <0, on compare avec $-t_{crit}$ pour conclure.
$\,$
- **Pairé ou non pairé?**
	***Pairé***: On compare les entrées unes à unes. Dans un tableau de valeurs, la valeur pour une entrée a un lien précis avec la valeur à côté.
	Exemples: 
	- *lien* extraversion entre le cadet et l'ainé (on compare le cadet avec son ainé - voir exercice 10.10). 
	- *avant/après* un traitement, un évènement, une période etc.
	***Non-pairé***: personnes différentes sans lien entre elles. On ne compare pas spécifiquement la personne à celle qui se trouve en face dans le tableau.
$\,$
- **Test sur une moyenne** ou **test sur 2 moyennes**?
	Test sur une moyenne: on compare un échantillon à une moyenne de la population
	Test sur deux moyennes: on compare deux échantillons entre eux (ex: 150 femmes, 148 hommes).

**Chapitre 1**: 
- **Décrivez**
	=> Utiliser $n$
$\,$
- **Inférez à partir de l'échantillon**
- **Estimez**
	=> Utiliser $n - 1$
$\,$
**Variables nominales**: genre, situation familiale, ...
**Variables ordinales**: âge, position dans un classement (1er, 2ème, ...), QI. Un QI de 70 n'est pas précisément 2x moins élevé qu'un QI de 140
**Variables métriques**: nombre de verres, poids, taille, revenu, nb. d'enfants,...

**Chapitre 2:**
- **Quelle est la variance de** "quelque chose" 
	- "**dans cet échantillon**" => formule de la variance en $n$
	- **sinon** = formule de la variance en $n-1$ **ou** mettre au carré le $S_x$ (la calculatrice utilise $n-1$ pour donner $S_x$)
- Si tu veux trouver l'écart type des valeurs dans un échantillon, utilises N-1 pour que ce soit corrigé et transposable à la population (voir formule $S$).
- Tu peux utiliser le $S$ de la calculatrice car il utilise la formule N-1 pour corriger et appliquer à une population.
---
**Chapitre 3**: 

- **Combien de fois plus de risque que**...,
- De **combien de fois augmente** le risque de ... chez les ...
	=> **Rapport de chances:** Par défaut on utilise le rapport de chances sauf si l'énoncé précise qu'il attend le risque relatif. $(A*D) / (B*C)$
$\,$
- Si on demande l'effet d'un critère parmi plusieurs (ie. incitation financière parmi envoi de SMS et "Rien") comparé à l'absence de celle-ci, on comparera à "Rien" et pas à la somme de "Rien" et "SMS" car SMS va biaiser l'observation qui ne porte que sur l'incitation financière.
$\,$
- **Estimez l'importance de la relation**,
- **Quel est le degré de relation**
	=> coefficient de corrélation ($r$) (résultat en proportion)
$\,$
- Quel est le **pourcentage de variabilité** de Y qui **est prédite par** la variabilité de X?
- Quel est le **taux**/part **de variabilité**/variance **entre** 2 variables - (/!\\ *plus de*, *moins de* x% de variabilité: test $t$ sur une corrélation)
	=> Coefficient de détermination $r^2$ (résultat en **%** + METTRE $r$ AU CARRÉ!!)
$\,$
- De **combien de points augmentent** les résultats de V1 (résultat cherché) **pour chaque point supplémentaire sur** V2 (prédicteur X). 
	=> Donner $b$.
$\,$
- Quelle est la **meilleure prédiction du score** de X d'une personne ayant souffert de Y?
	=> À défaut d'autre information, c'est la moyenne de l'échantillon qui constitue la meilleure estimation.
- Quelle est votre **meilleure prédiction du score** pour Y (VI) si une personne a eu un score de ... pour X?
	=> On calcule le $\hat{Y}$ avec la pente de régression.
$\,$
- **Autre formule de $r$**
	$r = b * \dfrac{S_X}{S_Y}$
- **Autre formule de** $b$
	$b = r * \dfrac{S_y}{S_x}$

--- 
**Chapitre 4:**
- **Importance de l'erreur d'estimation:**
	- erreur standard d'estimation: $S_{XY}$
		$S_Y$ est l'écart-type de la variable dépendante (pas le prédicteur X, l'autre)
	- valeur résiduelle: $S_{XY}^2$

---
**Chapitre 5:** 
- Ne pas confondre 
	- 10% (Z=1,28,  P=0,1) 
	- 1% (Z = 2,33, P=0,01)
$\,$
- Ne pas oublier le signe du Z score (en dessous ou au dessus de la moyenne)

---
**Chapitre 6:**
	**Erreur de 1ère espèce:** 
	"Je diagnostique une maladie mentale à un patient parce qu'il est dans les 5% (mais c'est une erreur). En réalité, c'était un sujet sain"
	**Erreur de 2ème espèce:**
	"Je ne diagnostique pas une maladie mentale à un patient alors qu'il est malade"
	($\alpha$ *trop petit? - peut-être que je l'aurais inclus dans les malades si j'avais été plus large et utilisé 0.05 au lieu de 0.01*)."
- Calculez la **probabilité de commettre une erreur de seconde espèce**
	1) Calculer d'abord la limite de rejet (trouver le X limite qui représente le 0.05) dans la population saine. Exemple: dans une population saine, le QI limite pour arriver dans les 5% est de 75 (valeur fictive).
	2) Utiliser ce X dans la population alternative (atteints d'une maladie) et chercher la probabilité que X > 75 (passer par le Z).
- **Estimez avec une certitude de 95%**
	- Intervalle de confiance (unilatéral ou bilatéral)

---
**Chapitre 7:** 
- Donnez la **taille de l'effet** de X sur Y
	- Choisir une mesure d'association après le Khi-carré
$\;$
- Y a t-il une **répartition** différente entre les catégories de l'échantillon **comparé à** des valeurs de référence d'**une population plus large**?
- **Les hommes sont-ils plus** représentés dans les professions médicales? **50-50%?**
	- *Khi-carré d'ajustement* (observé: échantillon, attendu: pop. référence)
	  Pas de VI + Variables nominale => Test Khi carré d'ajustement
	  Comparer valeurs observées et valeurs attendues avec la formule du Khi carré.
$\,$
- Peut-on affirmer que X **affecte la répartition** de Y?
- **Est-ce qu'il y a un lien entre** le comportement et la maladie?
- **La prévalence** de X **est-elle influencée par Y** (+variables nominales - i.e. genre/PTSD)?
	=> *Khi carré d'indépendance* + table des valeurs critiques + Voir les degrés d'association si rejet
	**Calculer les valeurs attendues**: voir la table plus bas.
	Pour les mesures d'associations:
	- Ne pas mettre Khi carré $\chi^2$ encore au carré, ...
	**VÉRIFIER LE CALCUL KHI CARRÉ!** (mise au carré, valeurs)
	L'hypothèse peut être formulée en français
	**Ligne ou colonne?**
	- "Il y a autant d'occurrences de X (ligne - aide/pas d'aide) dans les différents groupes (colonnes, Féminin/Masculin)"

Khi carré - comment calculer les valeurs attendues (**v. initiale** | $\text{v. attendue}$)

|                    | **Cancer**                                   | **Pas de cancer**                               |         |
| ------------------ | -------------------------------------------- | ----------------------------------------------- | ------- |
| **Rapide**         | **55** \| ($\dfrac{125}{500} * 125) = 31,25$ | **70** \|  ($\dfrac{125}{500} * 375) = 93,75$   | **125** |
| **Végé**           | **5**  \| ($\dfrac{50}{500} * 125) = 12,5$   | **45** \| ($\dfrac{50}{500} * 375) = 37,5$      | **50**  |
| **Traditionnelle** | **65** \| ($\dfrac{325}{500} * 125) = 81,25$ | **260**  \| ($\dfrac{325}{500} * 375) = 243,75$ | **325** |
|                    | **125**                                      | **375**                                         | **500** |

---
**Chapitre 8:**
- Ne pas confondre:
	- $\bar{X}$: échantillon
	- $\mu$: population
	  
	**Question impliquant une direction**:  "Peut-on affirmer une tendance accrue pour ..."
	$H_0: \mu = 20.31$ 
	$H_A: \mu > 20.31$
	on peut avoir un "$<$" ou "$>$" opposé à un "$=$" 
	$\text{}$
	$H_0$ se lit aussi "La moyenne de la population est une moyenne plausible pour la population alternative".
	
	**Quelle est la probabilité que la** "*taille, tolérance, ...*" ***moyenne*** d'un groupe de $n$ personnes soit supérieure/inférieure à ...
	Calculer le $Z$

---
**Chapitre 9:**
- **"Déterminer si il y a un changement avant/après"**:
	- test $t$ pour échantillons pairés

Test $t$ pour échantillons pairés:
-  test qui peut aussi être bilatéral ($\neq$ => $alpha/2$)
Test $t$ pour échantillons indépendants:
- Utiliser la variance et pas l'écart-type dans la formule du $t$!! => Mettre au carré!

---
**Chapitre 10:**
- Somme des rangs de Wilcoxon

| Valeurs        | 1                                              | 1   | 1   | 1   | 1   | 3   | 3   | 5   | 6   | 6   |
| -------------- | ---------------------------------------------- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Avec ex-aequos | 3                                              | 3   | 3   | 3   | 3   | 6,5 | 6,5 | 8   | 9,5 | 9,5 |
| Remarques      | Pour les 1, on obtient 3 car (1+2+3+4+5 )/5= 3 |     |     |     |     |     |     |     |     |     |

---
**Chapitre 11:**
- Peut-on affirmer que la **corrélation** entre X et Y est **de taille** moyenne?"
	=> "Test $t$ sur une corrélation" avec hypothèses
	
	Corrélation taille moyenne: $0,5 - 0,8$ => on prend la borne inférieure.
	
	$H0: \rho = 0,5$
	$HA:\rho > 0,5$
$\;$
- Peut-on affirmer que le score au CEB permet de **prédire** moins de **X% de la variance** sur le score du CESS ?
	=> Test $Z$ de corrélation pour 9% de variance 
	$H_0: \rho = 0,3\; (\sqrt{0,09)}$ (9% = 0,09)
	$H_0: \rho \lt 0,3\; (\sqrt{0,09)}$ (plus de X% = $\lt$, moins de X% = $\gt$)

- L’ancienneté **explique** 20,25% de **la variabilité observée** au niveau de la perception de la sécurité de l’emploi.
	=> Test sur une corrélation








# Synthèse Alice
![[462553764_1231463131474786_7688113640270818824_n.jpg]]

![[462559445_1048585096814616_962163564229406884_n.jpg]]

![[462549278_563474656236992_8603018799867739171_n.jpg]]

![[462566020_427312977065836_295481842384961289_n.jpg]]

![[462547960_581183161013760_6749134258138331621_n.jpg]]

![[462577569_540530568522784_9070010573457157622_n.jpg]]

![[462544291_570450518660000_2268473802902456002_n.jpg]]

![[462558137_1220476082622832_3810979414735390004_n.jpg]]

![[462546577_509571485238459_8747197142737270106_n.jpg]]

![[462544321_3658981274432707_1297408267300811024_n.jpg]]

![[462641842_557676866664318_3689968181899962546_n.jpg]]



![[462557213_509083161951579_4795374451997695839_n.jpg]]

![[462558161_1191784681898437_190148646554460040_n.jpg]]

![[462542498_432760779845809_767525753958859466_n.jpg]]

![[462557290_1065393581695389_5237059395075320471_n.jpg]]

![[462568957_597752946028382_4550873800518845053_n.jpg]]

![[462554056_1956677894835028_5133625274802216982_n.jpg]]

![[462543127_8541749552580174_1997168998760686539_n.jpg]]

![[462565446_8914698975249518_8548150580212168060_n.jpg]]

![[462568956_1733235254181900_7685534517502591342_n.jpg]]

![[462542543_844438101099785_5947405625262922105_n.jpg]]

![[462541066_899254738860339_4938514831427041839_n.jpg]]

![[462551942_1050146010123937_9202535158853543697_n.jpg]]

![[462547903_560112689825145_4284423608717052451_n.jpg]]




