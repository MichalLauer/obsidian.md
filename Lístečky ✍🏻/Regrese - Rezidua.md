---
Datum: 2024-03-09
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese/MLR 
# Regrese - Rezidua
Reziduální složka je v regresi definovaná jako
$$
e_i = y_i - \hat{y}_i.
$$
V určitých případech lze složku použít pro odhad [[Regrese - Chybová složka|chybové složky]], ale nemusí tomu být vždy tak. Pokud jsou u modelu porušeny silně předpoklady, je možné residua pro odhad transformovat. Další definice může být pomocí [[Regrese - Matice M|matice M]].
$$
\mathbb{e} = \mathbb{M}\mathbb{y} = \mathbb{M} \mathbb{\epsilon}
$$
**Očekávaná hodnota** za platnosti [[Regrese - Nezávislost residuí|nezávislosti residuí]] je
$$
E(\mathbb{e}) = \mathbb{M} E(\mathbb{\epsilon}) = 0,
$$
**kovarianční matice** pak za platnosti [[xRegrese - Homoskedasticita]] je
$$
C(\mathbb{e}) = \mathbb{M} C(\mathbb{e}) \mathbb{M}^T = \sigma^2 \mathbb{M}.
$$
Kovarianční matice pak vypadá jako
$$
C(\mathbb{e}) = 
\begin{bmatrix} 
\sigma^2(1 - h_{11}) & -\sigma^2h_{12}      & \dots \\
-\sigma^2h_{21}      & \sigma^2(1 - h_{22})  & \dots \\
\vdots               & \vdots                & \ddots
\end{bmatrix},
$$
obecně lze tedy **rozptyl** zapsat jako $\sigma^2(1 - h_{ii})$ a **kovariance** jako $-\sigma^2h_{ij}$.
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