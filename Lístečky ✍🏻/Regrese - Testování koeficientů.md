---
Datum: 2024-03-21
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Testování koeficientů
Odhad se řídí pravidly [[Regrese - Inference]].
$$
\frac{\frac{b_j - \beta_j}{\sigma \sqrt{a_{jj}}}}{\sqrt{\frac{(n-p)s^2(e)}{\sigma^2 (n-p)}}} =
\frac{b_j - \beta_j}{s(e) \sqrt{a_{jj}}} =
\frac{b_j - \beta_j}{s(b_j)} \sim t(n-p)
$$
Pokud by byl populační rozptyl $\sigma^2$ známý, koeficienty mají normální rozdělení.
$$
\frac{b_j - \beta_j}{\sigma\sqrt{a_{jj}}} \sim N(0, 1)
$$
### Simultánní oblast spolehlivost
Oblast pro všechny koeficienty najednou je definovaná jako
$$
\{ \mathbb\beta \in \mathbb R^p : (\mathbb\beta - \mathbb b)^T \mathbb X^T \mathbb X (\mathbb\beta - \mathbb b) \leq ps^2(e)F_{1 - \alpha}(p, n-p)\}
$$
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]