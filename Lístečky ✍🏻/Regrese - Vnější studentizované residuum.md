---
Datum: 2024-04-20
Typ:
  - Bibliografická
aliases:
  - Regrese - Jackknife residuum
---
*Klíčová slova:* #Regrese 
# Regrese - Vnější studentizované residuum
[[Regrese - Rezidua]] $e_{Ji}$ lze vypočítat z [[Regrese - Predikované residuum]] jako
$$
e_Ji = \frac{e_{i(-i)}}{s_{(-i)} (e) \left( x_i^T \left( X_{(-1)}^T X_{(-1)} \right)^{-1} x_i + 1 \right)}
$$
Pokud platí [[Regrese - Silná sada předpokladů]], potom
$$
e_{Ji} \sim T(n - p - 1).
$$
Pro zjednodušený výpočet lze získat $e_{Ji}$ jako
$$
e_{Ji} = \frac{e_i}{s_{(-i)}(e) \sqrt{1 - h_{ii}}},
$$
kde
$$
e_{(-i)} = \sqrt{\frac{(n-p)s^2(e) - e^2/(1 - h_{ii})}{n - p - 1}}.
$$
kde $h_{ii}$ značí [[Regrese - Leverage]]. Vnější studentizovaná residua lze tedy získat i z hlavního modelu bez použití predikovaného residua.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]