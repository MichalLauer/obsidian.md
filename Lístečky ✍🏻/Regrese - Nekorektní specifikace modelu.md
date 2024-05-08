---
Datum: 2024-05-08
Typ:
  - Bibliografická
aliases: #Regrese
---
*Klíčová slova:* 
# Regrese - Nekorektní specifikace modelu
Pokud je porušen [[Regrese - Předpoklad exogenity chyb]], model je nekorektně specifikovaný, jelikož
$$
E(\epsilon) \neq \mathbb 0 \implies E(y) \neq \mathbb X \beta.
$$
Toto nezabraňuje predikcím, které mohou být stále kvalitní a relativně dobré. Je to ale veliký problém pro provádění **inference**.

> [!warning] Průměr residuí
> Pro kontrolu **nelze** použít průměr residuí, t.j. $\sum(e) \ n$, jelikož ten se bude u metody MNČ s absolutním členem rovnat vždy nule.

## Grafické postupy
- porovnání (libovolných) residuí proti [[Regrese - Vyrovnané hodnoty]]
- porovnání residuí a vysvětlujících proměnných
- residua v jejich získaném pořadí

> [!hint] Propojení
> Pomocí postupů lze odhadnout i vlastnosti o konstantním rozptylu, normalitě chybové složky nebo nekorelovanost.


- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
