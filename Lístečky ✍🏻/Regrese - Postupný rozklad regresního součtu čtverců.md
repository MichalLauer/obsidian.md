---
Datum: 2024-04-20
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese 

> [!info] Platnost
> Platí pouze u [[Regrese - Metoda nejmenších čtverců]]
# Regrese - Postupný rozklad regresního součtu čtverců
Jelikož po přidání nové proměnné se může [[Součet vysvětlených čtverců|SSE]] pouze [[Regrese - Změny součtů čtverců|zvýšit]], lze vypočítat jeho celkové zvýšení po přidání $X_k$ jako
$$
Q(\hat y | X_1, \dots, X_k) - Q(\hat y | X_1, \dots, X_{k-1}).
$$
Celkový součet vysvětlených čtverců lze zapsat jako
$$
Q(\hat y | X_1, \dots, X_k) = Q(\hat y; X_1) +
\Delta Q(\hat y;X_2 | X_1) + \dots +
\Delta Q(\hat y;X_k | X_1, \dots, X_k).
$$
Pokud budou proměnné přidány v jiném pořadí, jejich $\Delta Q(\hat y)$ se ale změní. Proto je nutné vypočítat průměrný příspěvek přes všechny $k!$.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]