---
Datum: 2024-03-09
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Rezidua
Reziduální složka je v regresi definovaná jako
$$
e_i = y_i - \hat{y}_i.
$$
V určitých případech lze složku použít pro odhad [[Regrese - Chybová složka|chybové složky]], ale nemusí tomu být vždy tak. Pokud jsou u modelu porušeny silně předpoklady, je možné residua pro odhad transformovat. 
# Geometrická interpretace
Z [[Optimalizace - Metoda nejmenších čtverců|MNČ]] lze rozepsat residua do tvaru
$$
\mathbb{X}^Te = 0.
$$
Residua jsou tedy **kolmá na regresní matici**. Z toho také plyne, že suma součtu residuí a libovolné nezávislé proměnné je nulový.
$$
\sum_{i=1}^n x_{ij} e_i = 0, j = 1, \dots, k
$$
Toto také platí pro úhrn součtu vyrovnaných proměnných a residuí.
$$
\sum_{i=1}^n \hat{y}_i e_i = 0, j = 1, \dots, k
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]