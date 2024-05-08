---
Datum: 2023-12-27
Typ:
  - Bibliografická
aliases:
  - SST
---
*Klíčová slova:* #Metrika 
# Celkový součet čtverců
Celkový součet čtverců (SST) je součet čtvercových odchylek hodnoty od jejího průměru.
$$
\text{SST} = Q(y) = \sum_{i=1}^n (y_i - \overline{y})^2
$$
Lze vyjádřit i ve vztahu k [[Součet čtverců reziduí|SSR]] a [[Součet vysvětlených čtverců|SSE]], tedy
$$
\begin{align}
\text{SST} &= \sum_{i=1}^n (y_i - \overline{y})^2 \\
\text{SST} &= \sum_{i=1}^n ((y_i - \hat{y}_i) + (\hat{y}_i - \overline{y}))^2 \\
\text{SST} &= \sum_{i=1}^n ((y_i - \hat{y}_i)^2 + 2(y_i - \hat{y}_i)(\hat{y}_i - \overline{y}) + (\hat{y}_i - \overline{y})^2) \\
\text{SST} &= \text{SSR} + 2(y_i - \hat{y}_i)(\hat{y}_i - \overline{y}) + \text{SSE} \\
\text{SST} &= \text{SSR} + 2\sum_{i=1}^n \hat{u}_i(\hat{y}_i - \overline{y}) + \text{SSE}. \\
\end{align}
$$
> [!DANGER] Platnost
> Prostřední člen vypadne, pokud jsou residua a $\hat{y}$ nezávislá. Pokud nejsou, tento vztah neplatí  (Wooldridge 2020, s. 34). Také je nutné mít v regresním modelu absolutní člen (Malec 2024)

- - -
# Literatura
[[Wooldridge2020_IntroductoryEconometricsModern|WOOLDRIDGE, Jeffrey M., 2020. Introductory econometrics: a modern approach. Seventh edition. Boston, MA: Cengage. ISBN 978-1-337-55886-0.]]
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
