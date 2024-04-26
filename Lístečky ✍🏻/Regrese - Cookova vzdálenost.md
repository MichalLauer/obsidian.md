---
Datum: 2024-04-20
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese/AnalýzaResiduí
# Regrese - Cookova vzdálenost
Cookova vzdálenost ukazuje vliv daného pozorování.
$$
D_i = \frac{(\hat y_{(-i)} \hat y_i)^T (\hat y_{(-i)} \hat y_i)}{ps^2(e)}
$$
Hodnota $\hat y_{(-i)}$ označuje predikci $i$-tého pozorování na modelu, který byl natrénován na všech datech kromě $i$-tého. Pokud je hodnota $> 1$, dané pozorování může být vlivné.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]