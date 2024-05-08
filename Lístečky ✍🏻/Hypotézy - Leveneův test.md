---
Datum: 2024-05-08
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Hypotézy/Rozptyl 
# Hypotézy - Leveneův test
Testujeme, zda je populační rozptyl v $k$ skupinách stejný.
$$
\begin{align}
\text{H0}&: \sigma^2_1 = \sigma^2_2 = \dots = \sigma^2_k \\
\text{H1}&: \neg \text{H0}
\end{align}
$$
## Předpoklady
- Normalita dat
> [!tip] Náhrada
> Jako robustní náhrada se doporučuje [[Hypotézy - Brown-Forsythův test]]

- Rozptyly si jsou relativně blízko
## Princip
[[ANOVA]] test, který je proveden na absolutních hodnotách.

> [!NOTE] Aproximativní vztah
> Jelikož se absolutní hodnoty nejspíše nemají normální rozdělení, výsledky nejsou úplně přesné.

- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]