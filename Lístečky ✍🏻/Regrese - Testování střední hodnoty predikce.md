---
Datum: 2024-03-21
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Testování střední hodnoty predikce
Odhad se řídí pravidly [[Regrese - Inference]].
$$
\frac{\frac{x_*^Tb - x_*^T\beta}{\sigma \sqrt{x_*^T (\mathbb X^T \mathbb X)^{-1}x_*}}}
{\sqrt{\frac{(n-p)s^2(e)}{\sigma^2 (n-p)}}} =
\frac{x_*^Tb - x_*^T\beta}{s(e) \sqrt{x_*^T (\mathbb X^T \mathbb X)^{-1}x_*}} =
\frac{x_*^Tb - x_*^T\beta}{s(\hat\eta_*)} \sim t(n-p)
$$
## Interval spolehlivosti
$(1 - \alpha)*100\%$ oboustranný interval spolehlivosti pro střední hodnoty predikcí $x_*^T b$ lze definovat tedy jako
$$
x_*^Tb \pm t_{1 - \alpha}(n - p) s(\hat\eta_*)
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]