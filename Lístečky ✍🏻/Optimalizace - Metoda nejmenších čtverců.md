---
Datum: 2024-02-27
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Optimalizace
# Optimalizace - Metoda nejmenších čtverců
Součet nejmenších čtverců lze obecně zapsat jako
$$
\min \sum_{i=1}^n \epsilon^2 =
\min \sum_{i=1}^n (y_i - \hat{y})^2 =
\min \sum_{i=1}^n \left(y_i -\beta_0 - \beta_1x_1 - \dots - \beta_kx_k\right)^2,
$$
maticově pak
$$
\min \epsilon^T\epsilon =\sum_{i=1}^n (\mathbb{y} - \mathbb{X}\mathbb{\beta})^2.
$$
Kvadratický tvar výrazu lze dále rozepsat na
$$
\begin{align}
(\mathbb{y} - \mathbb{X}\mathbb{\beta})^2 
&= (\mathbb{y} - \mathbb{X}\mathbb{\beta})^T(\mathbb{y} - \mathbb{X}\mathbb{\beta}) \\
&= \mathbb{y}^T\mathbb{y} -
\mathbb{y}^T\mathbb{X}\mathbb{\beta} - 
\mathbb{\beta}^T\mathbb{X}^T\mathbb{y} + 
\mathbb{\beta}^T\mathbb{X}^T\mathbb{X}\mathbb{\beta} \space (1)\\ 
&= \mathbb{y}^T\mathbb{y} -
2\mathbb{\beta}^T\mathbb{X}^T\mathbb{y} + 
\mathbb{\beta}^T\mathbb{X}^T\mathbb{X}\mathbb{\beta}
\end{align}
$$
(1) jelikož $\mathbb{y}^T\mathbb{X}\mathbb{\beta}$ je skalár, lze ho celý transponovat na výraz $\mathbb{\beta}^T\mathbb{X}^T\mathbb{y}$
Výraz je poté nutné parciálně derivovat podle $\beta$.
$$
\frac{\partial (\mathbb{y} - \mathbb{X}\mathbb{\beta})^2}{\partial \beta} =
-2\mathbb{X}^T\mathbb{y} + 2\mathbb{X}^T\mathbb{X}\mathbb{\beta}
$$
Po zjednodušení vychází rovnice
$$
\mathbb{X}^T\mathbb{X}\mathbb{\beta}=\mathbb{X}^T\mathbb{y},
$$
odkud lze poslední úpravou vyjádřit $\mathbb{\beta}$.
$$
\mathbb{\beta}=\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T\mathbb{y},
$$
## Konzistence matice
Pokud existuje inverze $(\mathbb{X}^T\mathbb{X})^{-1}$, matice je konzistentní. To znamená, že existuje právě jedno řešení. V opačném případě (tedy neexistuje inverze) existuje perfektní lineární závislost mezi daty a metoda nelze použít.
# Implementace
Jelikož je hledání inverze velmi výpočetně náročné, na počítači se k získání řešení používá [[QR rozklad matice]].