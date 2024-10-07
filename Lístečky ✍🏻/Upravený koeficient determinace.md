---
Datum: 2024-06-01
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Metrika
# Upravený koeficient determinace
Jedná se o úpravu [[Koeficient determinace|koeficientu determinace]], který sám o sobě není vhodný pro porovnávání modelů s různými proměnnými (viz. [[Regrese - Změny součtů čtverců|Regrese - neklesající SSE]]).
$$
R^2_{\text{adj.}}
= 1 - \frac{Q(e)/(n-p)}{Q(y)/(n-1)}
= 1 - \frac{s^2(e)}{Q(y)/(n-1)}
= 1 - \frac{n-1}{n-p}\frac{Q(e)}{Q(y)}
$$
Poměr residuí je proto vážená 
1) počtem pozorování, a
2) počtem regresorů.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]