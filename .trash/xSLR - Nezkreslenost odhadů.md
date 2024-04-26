---
Datum: 2023-12-28
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Regrese/SLR
# SLR - Nezkreslenost
Pokud jsou splněné [[xSLR - Předpoklady]] SLR.1 - SLR.4, jsou odhady nezkreslené.
## Nezkreslenost $\hat{\beta}_1$
Koeficient lze získat jako
$$
\hat{\beta}_1 = \frac{\sum_{i=1}^n (x_i - \overline{x})(y_i - \overline{y})}{\sum_{i=1}^n (x_i - \overline{x})^2}.
$$
Pro jednodušší důkaz se čitatel převede pomocí [[Součin odchylek od průměru na součin odchylky a hodnoty]] na
$$
\hat{\beta}_1 = \frac{\sum_{i=1}^n (x_i - \overline{x})y_i.}{\sum_{i=1}^n (x_i - \overline{x})^2},
$$
pomocí kterého pak lze ukázat, že
$$
\begin{align}
\hat{\beta}_1 &= \frac{\sum_{i=1}^n (x_i - \overline{x})y_i}{\sum_{i=1}^n (x_i - \overline{x})^2} \\
&= \frac{\sum_{i=1}^n (x_i - \overline{x})(\beta_0 + \beta_1x_i + u_i)}{\sum_{i=1}^n (x_i - \overline{x})^2} \\
&= \frac{\beta_0\sum_{i=1}^n (x_i - \overline{x}) + \beta_1\sum_{i=1}^n (x_i - \overline{x})x_i + \sum_{i=1}^n (x_i - \overline{x})u_i}{\sum_{i=1}^n (x_i - \overline{x})^2} \\
&= \frac{0 + \beta_1\sum_{i=1}^n (x_i - \overline{x})^2 + \sum_{i=1}^n (x_i - \overline{x})u_i}{\sum_{i=1}^n (x_i - \overline{x})^2} \\
&= \beta_1 + \frac{\sum_{i=1}^n (x_i - \overline{x})u_i}{\sum_{i=1}^n (x_i - \overline{x})^2}. \\
\end{align}
$$
Pokud z výrazu vezmeme očekávanou hodnotu $E(\cdot)$, poté
$$
\begin{align}
E(\hat{\beta}_1) &= E\left(\beta_1 + \frac{\sum_{i=1}^n (x_i - \overline{x})u_i}{\sum_{i=1}^n (x_i - \overline{x})^2}\right) \\
&= \beta_1 + E\left(\frac{\sum_{i=1}^n (x_i - \overline{x})u_i}{\sum_{i=1}^n (x_i - \overline{x})^2}\right) \\
&= \beta_1,
\end{align}
$$
jelikož $E(u_i) = 0$ ([[xSLR - Předpoklad SLR.3]]), odhad je nezkreslený.
## Nezkreslenost $\hat{\beta}_0$
Pro nezkreslenost parametru $\hat{\beta}_0$ lze převést na
$$
\begin{align}
\hat{\beta}_0 &= \overline{y} - \hat{\beta}_1\overline{x} \\
&= (\beta_0 + \beta_1\overline{x}) - \hat{\beta}_1\overline{x} \\
&= \beta_0 + \overline{x}(\beta_1 - \hat{\beta}_1). \\
\end{align}
$$
Očekávaná hodnota je pak
$$
\begin{align}
E\left(\hat{\beta}_0\right) &= \left(\beta_0 + \overline{x}(\beta_1 - \hat{\beta}_1)\right) \\
&= \beta_0,
\end{align}
$$
jelikož $\beta_1 - \hat{\beta}_1 = 0$.