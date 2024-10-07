---
Datum: 2024-03-23
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Metoda maximální věrohodnosti
Odhad pomocí maximální věrohodnosti lze použít pouze v případě, že data splňují [[Regrese - Silná sada předpokladů|silnou sadu předpokladů]].
## Odhad koeficientů
Pokud jsou splněné předpoklady, chyba modelu má normální rozdělení.
$$
\epsilon \sim NID(\mathbb 0, \sigma^2 I), \space
\epsilon_i \sim N(0, \sigma^2)
$$
Díky tomu lze zapsat hustotu chyby pomocí hustoty [[Rozdělení - Normální rozdělení|normálního rozdělení]].
$$
f(\epsilon) =
\frac{1}{\sigma\sqrt{2\pi}} \exp\left(\frac{-\epsilon^2}{2\sigma^2}\right)
$$
Z hustoty lze získat [[Věrohodnostní funkce]].
$$
L(\epsilon) = \Pi_{i=1}^n \frac{1}{\sigma\sqrt{2\pi}} \exp\left(\frac{-\epsilon_i^2}{2}\right) =
\left(\sigma^22\pi\right)^{-n/2} \exp \left(\frac{-\sum_{i=1}^n\epsilon_i^2}{2\sigma^2}\right) 
$$
Funkci je možné dále převést na [[Logaritmický věrohodnostní funkce]].
$$
LL(\epsilon) = \log\left(L(\epsilon)\right) =
\frac{-n}{2}\log(\sigma^22\pi) - \frac{\sum_{i=1}^n\epsilon_i^2}{2\sigma^2}
$$
Chyba $\epsilon_i = y_i - x_i\beta$. Po dosazení a derivace vzhledem k parametru $\beta$ dostáváme
$$
\frac{\partial LL}{\partial \beta} = - 
\frac{1}{2\sigma^2} 2\sum_{i=1}^n (y_i - x_i\beta) (-\sum_{i=1}^n x_i) = \frac{1}{\sigma^2} \sum_{i=1}^n x_i (y_i - x_i\beta).
$$
Teď stačí derivaci položit rovno nule a získat tam maximum.
$$
\begin{align}
\frac{1}{\sigma^2} \sum_{i=1}^n x_i (y_i - x_i\beta) &= 0 \\
\sum_{i=1}^n x_iy_i - \beta\sum_{i=1}^n x_i^2 &= 0 \\
\sum_{i=1}^n x_iy_i &= \beta\sum_{i=1}^n x_i^2
\end{align}
$$
Pokud se odhad přepíše do maticového zápisu, získáváme
$$
\begin{align}
\sum_{i=1}^n x_iy_i &= \beta\sum_{i=1}^n x_i^2 \\
\mathbb X^T \mathbb y = (\mathbb X^T \mathbb X)\beta \\
(\mathbb X^T \mathbb X)^{-1} \mathbb X^T \mathbb y &= \beta.
\end{align}
$$
## Odhad rozptylu
Vycházejme ze stejné logaritmické věrohodnostní funkce
$$
LL(\epsilon) =
\frac{-n}{2}\log(\sigma^22\pi) - \frac{\sum_{i=1}^n\epsilon_i^2}{2\sigma^2}
= \frac{-n}{2}\log(\sigma^2) - \frac{n}{2}\log(2\pi) - \frac{\sum_{i=1}^n\epsilon_i^2}{2\sigma^2}
$$
Pokud ji budeme derivovat vzhledem k $\sigma^2$ dostáváme
$$
\frac{\partial LL}{\partial \sigma^2} =
\frac{-n}{2\sigma^2} - \frac{\sum_{i=1}^n\epsilon_i^2}{-2\sigma^{4}} =
\frac{-n}{2\sigma^2} + \frac{\sum_{i=1}^n\epsilon_i^2}{2\sigma^{4}}.
$$
Položením rovné nule a vyjádřením $\sigma^2$ lze dostat maximálně věrohodný estimátor.
$$
\begin{align}
\frac{-n}{2\sigma^2} + \frac{\sum_{i=1}^n\epsilon_i^2}{2\sigma^{4}} &= 0 \\
\frac{\sum_{i=1}^n\epsilon_i^2}{2\sigma^{4}} &= \frac{n}{2\sigma^2} \\
\frac{\sum_{i=1}^n\epsilon_i^2}{\sigma^2} &= n \\
\frac{\sum_{i=1}^n\epsilon_i^2}{n} &= \sigma^2.
\end{align}
$$

> [!important] Zkreslenost
> Odhad je pouze **asymptoticky nezkreslený**, protože neobsahuje korekci $n - k$.

- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
