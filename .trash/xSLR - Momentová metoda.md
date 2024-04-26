---
Datum: 2023-12-27
Typ:
  - Permanentní
---
*Klíčová slova:* #Regrese/SLR  #Estimátor 
# JRM - [[Momentová metoda]]
Pro odhad je možné využít [[JRM - Předpoklady|předpoklady]] a rovnice
$$
\begin{align}
E(u) = 0 &\implies E(y - \hat{\beta}_0 - \hat{\beta}_1x) = 0\text{, a} \\
E(xu) = 0 &\implies E(x(y-\hat{\beta}_0 - \hat{\beta}_1x)) = 0.
\end{align}
$$
Po převedení $E(\cdot)$ na $\frac{1}{n}(\cdot)$ a zbydou rovnice
$$
\begin{align}
\frac{1}{n} \sum_{i=1}^n \left(y_i - \hat{\beta}_0 - \hat{\beta}_1x_i \right) &= 0\text{, a} \\
\frac{1}{n} \sum_{i=1}^n  \left(x_i(y_i - \hat{\beta}_0 - \hat{\beta}_1x_i)\right) &= 0.
\end{align}
$$
Suma lze dále rozepsat a získáváme soustavu rovnic
$$
\begin{align}
\overline{y} - \hat{\beta}_0 - \hat{\beta}_1\overline{x} &= 0\text{, a} \\
\frac{\sum_{i=1}^n x_iy_i}{n} - \hat{\beta}_0\overline{x} - \hat{\beta}_1\overline{x^2}&= 0.
\end{align}
$$
Vyjádřením $\hat{\beta}_0$ z první rovnice získáváme $\hat{\beta}_0 = \overline{y} - \hat{\beta}_1\overline{x}$ a dosazením do druhé rovnice získáváme
$$
\begin{align}
\frac{\sum_{i=1}^n x_iy_i}{n} - \left[\overline{y} - \hat{\beta}_1\overline{x}\right]\overline{x} - \hat{\beta}_1\overline{x^2}&= 0 \\
\frac{\sum_{i=1}^n x_iy_i}{n} - \overline{y}\overline{x} + \hat{\beta}_1\overline{x}^2 - \hat{\beta}_1\overline{x^2}&= 0 \\
\frac{\sum_{i=1}^n x_iy_i - \sum_{i=1}^n x_i \sum_{i=1}^n y_i}{n} - \hat{\beta}_1var(X)&= 0 \\
COV(x, y) - \hat{\beta}_1VAR(x)&= 0 \\
\hat{\beta}_1 = \frac{COV(x, y)}{VAR(x)} = \frac{\sum_{i=1}^n (x_i - \overline{x})(y_i - \overline{y})}{\sum_{i=1}^n (x_i - \overline{x})^2}.
\end{align}
$$
Rozptyl je získán díky [[Rozptyl - Pomocí očekávaných hodnot]] a kovariance díky [[Součin odchylek od průměru na rozdíl úhrnů]]. Díky získanému odhadu $\hat{\beta_1}$ lze jednoduše dopočítat $\hat{\beta_0}$.
$$
\overline{y} - \hat{\beta}_0 - \hat{\beta}_1\overline{x} = 0
\implies
\hat{\beta}_0 = \overline{y} - \hat{\beta}_1\overline{x}
$$

> [!success] Finální odhady
> $\hat{\beta}_1 = \frac{COV(x, y)}{VAR(x)} = \frac{\sum_{i=1}^n (x_i - \overline{x})(y_i - \overline{y})}{\sum_{i=1}^n (x_i - \overline{x})^2}$
> $\hat{\beta}_0 = \overline{y} - \hat{\beta}_1\overline{x}$

- - -
# Literatura

