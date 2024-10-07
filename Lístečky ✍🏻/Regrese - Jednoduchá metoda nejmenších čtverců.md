---
Datum: 2023-12-27
Typ:
  - Permanentní
---
*Klíčová slova:* #Regrese
# Regrese - Jednoduchá metoda nejmenších čtverců
V případě [[Regrese - Jednoduchý regresní model]] lze jednoduše koeficient $b$ vyjádřit analyticky pomocí [[Optimalizace - Metoda nejmenších čtverců]]. Platí zde stejné předpoklady a vlastnost jako u [[Regrese - Metoda nejmenších čtverců]].
## Odhad $b_1$
$$
\min SSR =\min \sum_{i=1}^n (y_i - \hat{y}_i)^2 = \min (y_i-\hat{\beta}_0-\hat{\beta}_1x_i)^2
$$
Řešením jsou parciální derivace podle jednotlivých parametrů.
$$
\begin{align}
\frac{\partial SSR}{\partial \hat{\beta}_0} &= -2\sum_{i=1}^n(y_i-\hat{\beta}_0-\hat{\beta}_1x_i) = 0\\
\frac{\partial SSR}{\partial \hat{\beta}_1} &= -2\sum_{i=1}^nx_i(y_i-\hat{\beta}_0-\hat{\beta}_1x_i) = 0\\
\end{align}
$$
Řešením je tedy soustava rovnic
$$
\begin{align}
\sum_{i=1}^n (y_i-_0-\hat{\beta}_1x_i) &= 0\\
\sum_{i=1}^n x_i(y_i-\hat{\beta}_0-\hat{\beta}_1x_i) &= 0.
\end{align}
$$
Pro zjednodušení lze obě strany vynásobit $1/n$ a tím počítat s průměry, tedy
$$
\begin{align}
\frac{1}{n} \sum_{i=1}^n \left(y_i - \hat{\beta}_0 - \hat{\beta}_1x_i \right) &= 0\text{, a} \\
\frac{1}{n} \sum_{i=1}^n  \left(x_i(y_i - \hat{\beta}_0 - \hat{\beta}_1x_i)\right) &= 0.
\end{align}
$$Vyjádřením $\hat{\beta}_0$ z první rovnice získáváme $\hat{\beta}_0 = \overline{y} - \hat{\beta}_1\overline{x}$ a dosazením do druhé rovnice získáváme
$$
\begin{align}
\frac{\sum_{i=1}^n x_iy_i}{n} - \left[\overline{y} - \hat{\beta}_1\overline{x}\right]\overline{x} - \hat{\beta}_1\overline{x^2}&= 0 \\
\frac{\sum_{i=1}^n x_iy_i}{n} - \overline{y}\overline{x} + \hat{\beta}_1\overline{x}^2 - \hat{\beta}_1\overline{x^2}&= 0 \\
\frac{\sum_{i=1}^n x_iy_i - \sum_{i=1}^n x_i \sum_{i=1}^n y_i}{n} - \hat{\beta}_1var(X)&= 0 \\
COV(x, y) - \hat{\beta}_1VAR(x)&= 0 \\
\hat{\beta}_1 = \frac{COV(x, y)}{VAR(x)} = \frac{\sum_{i=1}^n (x_i - \overline{x})(y_i - \overline{y})}{\sum_{i=1}^n (x_i - \overline{x})^2}.
\end{align}
$$
## Odhad  $b_0$
Rozptyl je získán díky [[Rozptyl - Pomocí očekávaných hodnot]] a kovariance díky [[Kovariance - Pomocí souhrnů]]. Díky získanému odhadu $\hat{\beta_1}$ lze jednoduše dopočítat $\hat{\beta_0}$.
$$
\overline{y} - \hat{\beta}_0 - \hat{\beta}_1\overline{x} = 0
\implies
\hat{\beta}_0 = \overline{y} - \hat{\beta}_1\overline{x}
$$
> [!success] Finální odhady
> $\hat{\beta}_1 = \frac{COV(x, y)}{VAR(x)} = \frac{\sum_{i=1}^n (x_i - \overline{x})(y_i - \overline{y})}{\sum_{i=1}^n (x_i - \overline{x})^2}$
> $\hat{\beta}_0 = \overline{y} - \hat{\beta}_1\overline{x}$

## Rozptyl $\hat\beta_1$
Jelikož se 
$$
\hat{\beta}_1 = \beta_1 + \frac{\sum_{i=1}^n (x_i - \overline{x})u_i}{\sum_{i=1}^n (x_i - \overline{x})^2},
$$
potom lze získat rozptyl jako
$$
\begin{align}
VAR(\hat{\beta}_1) &= VAR\left(\beta_1 + \frac{\sum_{i=1}^n (x_i - \overline{x})u_i}{\sum_{i=1}^n (x_i - \overline{x})^2}\right) \\
&= VAR\left(\frac{u_i}{\sum_{i=1}^n (x_i - \overline{x})}\right) \\ 
&= \frac{1}{\sum_{i=1}^n (x_i - \overline{x})^2} VAR\left(\sum_{i=1}^n u_i\right) \\ 
&= \frac{\sigma^2}{\sum_{i=1}^n (x_i - \overline{x})^2}
= \frac{\sigma^2}{\text{SST}_x}
\end{align}
$$
## Rozptyl $\hat\beta_0$
Koeficient $\hat\beta_0$ lze zapsat jako 
$$
\hat{\beta}_0 = \overline{y} - \hat{\beta}_1\overline{x},
$$
a tedy rozptyl je
$$
\begin{align}
VAR(\hat{\beta}_0) &= VAR\left(\overline{y} - \hat{\beta}_1\overline{x}\right) \\
&= VAR\left(\overline{y}\right) + \left(\hat{\beta}_1\overline{x}\right) \\ 
&= \frac{1}{n^2} \sum_{i=1}^n Var(y_i) + \overline{x}^2Var(\hat\beta_1) \\
&= \frac{1}{n^2} n\sigma^2 + \overline{x}^2\frac{\sigma^2}{\text{SST}_x} \\
&= \sigma^2 \left( \frac{1}{n} + \frac{\overline{x}^2}{ \text{SST}_x} \right) \\
&= \sigma^2 \left( \frac{n^{-1}\text{SST}_x}{\text{SST}_x} + \frac{\overline{x}^2}{\text{SST}_x} \right) \\
&= \sigma^2 \left( \frac{n^{-1}\sum_{i=1}^n (x_i - \overline{x})^2 + \overline{x}^2}{\text{SST}_x} \right) \\
&= \sigma^2 \left( \frac{n^{-1}\sum_{i=1}^n (x_i^2 - 2x_i\overline{x} + \overline{x}^2) + \overline{x}^2}{\text{SST}_x} \right) \\
&= \sigma^2 \left( \frac{(n^{-1}\sum_{i=1}^n x_i^2 - 2\overline{x}n^{-1}\sum_{i=1}^n x_i + \overline{x}^2) + \overline{x}^2}{\text{SST}_x} \right) \\
&= \sigma^2 \left( \frac{n^{-1}\sum_{i=1}^n x_i^2 - 2\overline{x}^2 + 2\overline{x}^2}{\text{SST}_x} \right) \\
&= \frac{\sigma^2n^{-1}\sum_{i=1}^n x_i^2}{\text{SST}_x}  \\
\end{align}
$$
