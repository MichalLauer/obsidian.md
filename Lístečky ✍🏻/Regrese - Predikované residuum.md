---
Datum: 2024-04-20
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese 
# Regrese - Predikované residuum
Pro analýzu residuí lze porovnat $i$-té residuum z **plného modelu** s residuem predikované $i$-té hodnoty z modelu, který na $i$-té hodnotě nebyl natrénován.
$$
e_{i(-i)} = y_i - y_{i(-i)}
$$
Modely se nemusí počítat, ale platí vztah
$$
e_{i(-i)} = \frac{e_i}{1 - h_{ii}}.
$$
Pro predikovaná residua platí
$$
\begin{align}
E(e_{i(-i)}) &= 0 \\
D(e_{i(-i)}) &= \frac{D(e_i)}{(1 - h_{ii})^2} =
\frac{\sigma^2 (1 - h_{ii})}{(1 - h_{ii})^2} =
\frac{\sigma^2}{1 - h_{ii}}.
\end{align}
$$
Rozptyl lze také zapsat jako $\sigma^2 \left( x_i^T \left( X_{(-1)}^T X_{(-1)} \right)^{-1} x_i + 1 \right)$. 
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]