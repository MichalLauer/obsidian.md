---
Datum: 2024-03-21
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Testování predikce
Odhad se řídí pravidly [[Regrese - Inference]].
$$
\frac{\frac{y_* - x_*^Tb}{\sigma \sqrt{1 + x_*^T (\mathbb X^T \mathbb X)^{-1}x_*}}}
{\sqrt{\frac{(n-p)s^2(e)}{\sigma^2 (n-p)}}} =
\frac{y_* - x_*^Tb}{s(e) \sqrt{1 + x_*^T (\mathbb X^T \mathbb X)^{-1}x_*}} =
\frac{y_* - x_*^Tb}{s(y_* - \hat y_*)} \sim t(n-p)
$$
## Interval spolehlivosti
$(1 - \alpha)*100\%$ oboustranný interval spolehlivosti pro střední hodnoty predikcí $x_*^T b$ lze definovat tedy jako
$$
x_*^Tb \pm t_{1 - \alpha}(n - p) s(y_* - \hat y_*)
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]