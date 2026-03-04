![[Chapitre 3_stat2.pdf]]

La comparaison multiple s'applique à plusieurs types d'anovas, vus dans le chapitre 2 mais s'applique aussi à d'autres anovas qu'on verra dans les chapitres suivants. 

Si on voit des différences de moyennes, ce que l'on peut affirmer avec le rejet de $H_0$, les comparaisons multiples permettent de savoir à quels endroits sont les différences qu'on a repéré.
$H_0: µ1 = µ2 = µ3$
$H_a: µ1 \neq µ2 \neq µ3$ <= imaginons que ce soit validé par l'anova
Ok mais quel groupe est différent du quel? L'anova nous dit qu'au moins un des groupes est différent des autres. La comparaison des moyennes nous permet d'identifier quel(s) groupe(s) est différent de l'autre.

EC: taux de faux positifs par comparaison (1 comparaison entre 2 groupes)
EE: Erreurs de l'ensemble: probabilité d'avoir au moins une erreur pour l'ensemble (tous les groupes). Donc plus grands  (toutes les comparaisons entre tous les groupes).

EC < EE: EC sera toujours plus petit que EE.

$EE = 1-(1-EC)^C$
$(1-0,05) * (1-0,05) * (1-0,05) * (1-0,05) * ....$ 
=> où $C$ = nombre de groupes
=> où $...^C$ = probabilité d'avoir une erreur pour tous les C groupes

$EE = 1 - (1-0,05)^{10} = 0,40$ (où EC = 5% = 0,05)


**Comparer les moyennes 2 à 2**
Avantages: Aucune différence intéressante n'est négligée
Inconvénient: Beaucoup de comparaisons donc moins de puissance
Les chercheurs préfèrent garder tout que de perdre la puissance. 

La comparaison post-hoc ne sont pas assez souvent utilisées mais peuvent lêtre si on fait des hypothèses où on suppose des différences entre des groupes. 

# Exemple
5 groupes pour tester le sevrage tabagique:
- témoin
- Entrevue 
  effets non-spécifiques: simple fait de rencontrer un psychologue peut déjà être suffisant
- Technique de gestion
- Patch
- Traitement combiné (gestion + patch)

VD = nombre de jours de sevrage


Test t pour comparer 2 groupes: on modifie juste l'alpha en fonction du nombre de comparaisons qu'on va faire.

EE = c x EC
EC = EE / C

Je travaille avec un alpha qui est l'alpha de départ divisé par le nombre de comparaisons que je veux faire. 
Si mon alpha désiré pour l'ensemble (EE) est de 0,5 mais que je travaille avec 10 groupes, je vais utiliser un $EC = 0,05/10 = 0,005$

Le test de Dunn-Bonferroni ($t'$). si on n'a qu'une comparaison à faire, on peut utiliser la table de test $t$ classique (car la table $t'$ commence à 2). On devra alors se poser la question du test bilatéral ou unilatéral. Si > 1 comparaison, on utilisera TOUJOURS des tests bilatéraux 
$t^{\prime}=\frac{\overline{X}_1-\overline{X}_2}{\sqrt{CM_{erreur}\left(\frac{1}{n_1}+\frac{1}{n_2}\right)}}$


Ils font des hypothèses de supériorité entre des groupes
- Entrevue > témoins
- combiné > témoin
- combiné > gestion
- gestion > patch
1) $µ_{témoin} = \mu_{entrvue}$
2)  $µ_{combiné} = \mu_{témoin}$
3) ...
4) ...

On va faire 4 comparaisons
EE = 0,05
dl = 40

$t'_{0,05;40}=2,62$
$t'_{obs} $ devra être supérieur à 2,62.


Note: Si tous les groupes ont le même nombre de sujets, le dénominateur sera le même à chaque fois, pour les 4 tests (rappel: on fait 4 comparaisons ici).

Test 1: $t'$ ici est de 2,78 (>2,62.). On peut donc rejeter l'hypothèse nulle et considérer que la différence est significative. 

Test 2: $t'$ ici est de 7,73 (> 2,62.). On peut donc rejeter l'hypothèse nulle et considérer que la différence est significative. 

Test 3: ...

Plus on rajoutera des comparaisons (ici 4), plus les valeurs critiques seront sévères et plus on approchera de la possibilité de ne plus pouvoir affirmer $H_a$. On perdra donc en puissance. 