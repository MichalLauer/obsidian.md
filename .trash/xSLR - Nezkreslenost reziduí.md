---
Datum: 2023-12-30
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Regrese/SLR #Estimátor 
# SLR - Nezkreslenost reziduí
Pro nezkreslenost je vhodné si uvědomit, že $\hat u_i = y_i - \hat y_i = u_i - (\hat\beta_0 - \beta_0) - (\hat\beta_1 - \beta_1)x_1$, což vychází ze [[Regrese - Výběrový regresní model]] a [[Regrese - Výběrová regresní funkce]]. Pokud bychom vzali průměrné pozorování, pak $0 = \overline u - (\hat\beta_0 - \beta_0) - (\hat\beta_1 - \beta_1)\overline x$.  Po odečtený obou rovnic dostáváme
$$
\hat u_i - 0 = \left[u_i - (\hat\beta_0 - \beta_0) - (\hat\beta_1 - \beta_1)x_1\right] 
-
\left[\overline u - (\hat\beta_0 - \beta_0) - (\hat\beta_1 - \beta_1)\overline x \right]
$$
což se zjednoduší na 
$$
\hat u_i = (u_i - \overline u) - (\hat\beta_1 - \beta_1)(x_i - \overline x).
$$
Po dosazení výrazu do [[Součet čtverců reziduí|SSR]] dostáváme 
$$
\begin{align}
\text{SSR} &= \sum_{i=1}^n \hat u_i^2 \\
&= \sum_{i=1}^n (u_i - \overline u)^2 - 2(u_i - \overline u)(\hat\beta_1 - \beta_1)(x_i - \overline x) + (\hat\beta_1 - \beta_1)^2(x_i - \overline x)^2 \\
&= \sum_{i=1}^n (u_i - \overline u)^2 - 2(\hat\beta_1 - \beta_1)\sum_{i=1}^n(x_i - \overline x)u_i + (\hat\beta_1 - \beta_1)^2\sum_{i=1}^n(x_i - \overline x)^2.
\end{align}
$$
Aplikováním $E(\cdot)$ vychází
$$
\begin{align}
E(\text{SSR})
&= E \left(\sum_{i=1}^n (u_i - \overline u)^2 - 2(\hat\beta_1 - \beta_1)\sum_{i=1}^n(x_i - \overline x)u_i + (\hat\beta_1 - \beta_1)^2\sum_{i=1}^n(x_i - \overline x)^2 \right) \\
&= (n-2)\sigma^2
\end{align}
$$

> [!DANGER] Postup
> Důkaz moc nechápu tbh

> [!success] Finální odhady
> $E(\hat{\sigma}^2) = \frac{\sigma^2}{\text{SST}_x}$