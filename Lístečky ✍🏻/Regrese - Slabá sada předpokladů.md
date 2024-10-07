---
Datum: 2024-03-09
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese

> [!important] 
> Též [[Regrese - Gauss-Markův teorém]]
# Regrese - Slabá sada předpokladů
Slabá sada předpokladů obsahuje tři základní myšlenky o [[Regrese - Chybová složka|chybové složce]] regresního modelu. Pokud jsou předpoklady splněné, implikuje to určité vlastnosti o závislé složce.
## Předpoklady
1) **Střední hodnota** chybové složky je 0 (též [[Regrese - Předpoklad exogenity chyb]])
$$
E(\epsilon_i) = 0, i = 1, 2, \dots, n
$$
2) **Rozptyl** chybové složky je konstantní (též [[Regrese - Předpoklad homoskedasticity]])
$$
D(\epsilon_i) = \sigma^2 < \infty, i = 1, 2, \dots, n
$$
3) **Nekorelovanost** chybové složky.
$$
C(\epsilon_i, \epsilon_j) = 0; i \neq j, i = 1, \dots, n, j = 1, \dots, n
$$
## Implikace
Platnost předpokladů implikuje následující vlastnosti:
$$
\begin{align}
E(y_i) &= \eta_i \\
D(y) &= \sigma^2 \\
C(y_i, y_j) &= 0
\end{align}
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
