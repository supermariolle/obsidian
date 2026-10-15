![[Exercices Leçon 1(1).pdf]]

**==Données brutes:==**
``` sas
data scores;
input score1-score3;
datalines;
3 4 2
4 5 1
2 0 3
0 2 4 
3 5 1 
1 2 3
0 1 0
5 4 5
1 0 1
;
proc print data=scores noobs;
run;
```
