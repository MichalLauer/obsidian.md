---
Datum: 2024-04-20
Typ:
  - Bibliografická
aliases:
  - Regrese - Predicted residual sum of squares
---
*Klíčová slova:* #Regrese
# Regrese - PRESS
Metoda PRESS *(Predicted residual sum of squares)* slouží k porovnání různých modelů pomocí [[Regrese - Predikované residuum|predikovaných residuí]].
$$
Q(e_{(-i)}) = \sum_{i=1}^n e^2_{i(-i)}
$$
Modely s menším celkovým součtem budou pro predikci vhodnější. V podstatě se jedná o podobnou strategii v [[Křížová validace - leave-one-out]]. Pro vyhodnocení vhodnosti jednoho modelu lze použít 
$$
Q(e_{(-i)})/Q(e).
$$ Hodnoty větší než 1 naznačují, že v modelu existuje několik odlehlých pozorování.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]