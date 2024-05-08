---
Datum: 2024-03-23
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:*  #Regrese
# Regrese - Gauss-Markův teorém
Pokud je dodrženo pět základních předpokladů pro regresi, tedy
- [[Regrese - Předpoklad linearity]],
- [[Regrese - Předpoklad náhodného výběru]],
- [[Regrese - Předpoklad plné hodnosti]],
- [[Regrese - Předpoklad exogenity chyb]], a
- [[Regrese - předpoklad homoskedasticity]],
odhady pomocí [[Regrese - Metoda nejmenších čtverců]] jsou [[BLUE]]. Ve statistice také mluvíme o [[Regrese - Silná sada předpokladů]].
# Důkaz
Nejprve je nutné si definovat **obecný lineární** estimátor.
$$
b^0 = d + \mathbb L\mathbb y, \space
\mathbb L = (\mathbb X^T \mathbb X)^{-1} \mathbb X^T + D
$$
Jeho očekávaná hodnota je
$$
\begin{align}
b^0 &= d + \left[(\mathbb X^T \mathbb X)^{-1} \mathbb X^T + \mathbb D\right] \mathbb X \beta = 
b^0 = d + \beta + \mathbb D \mathbb X \beta \\
E(b^0) &= \beta.
\end{align}
$$
Tedy aby byl obecný odhad nezkreslený, musí platit to, že $\space \mathbb D \mathbb X = 0$ a $d = 0$.
**Rozptyl** tohoto odhadu je
$$
\begin{align}
C(b^0) &= C(\left[(\mathbb X^T \mathbb X)^{-1} \mathbb X^T + \mathbb D\right]\mathbb y) \\
&= \left[(\mathbb X^T \mathbb X)^{-1} \mathbb X^T + \mathbb D\right] \sigma^2 \left[(\mathbb X^T \mathbb X)^{-1} \mathbb X^T + \mathbb D\right]^T \\
&= \sigma^2 \left[(\mathbb X^T \mathbb X)^{-1} \mathbb X^T + \mathbb D\right] \left[\mathbb D^T + \mathbb X(\mathbb X^T \mathbb X)^{-1}\right] \\
&= \sigma^2 \left[ (\mathbb X^T \mathbb X)^{-1} \mathbb X^T \mathbb D^T + (\mathbb X^T \mathbb X)^{-1} + \mathbb D \mathbb D^T + \mathbb D \mathbb X (\mathbb X^T \mathbb X)^{-1} \right] \\
&= \sigma^2 \left[ (\mathbb X^T \mathbb X)^{-1} \left(\mathbb D \mathbb X\right)^T + (\mathbb X^T \mathbb X)^{-1} + \mathbb D \mathbb D^T + \mathbb D \mathbb X (\mathbb X^T \mathbb X)^{-1} \right] \\
&= \sigma^2 \left[ (\mathbb X^T \mathbb X)^{-1} + \mathbb D \mathbb D^T \right]
\end{align}
$$
Nyní je tedy nutné zjistit rozdíl obecného rozptylu a rozptylu OLS.
$$
A = C(b^0) - C(b) =
\sigma^2 \left[ (\mathbb X^T \mathbb X)^{-1} + \mathbb D \mathbb D^T \right] -
\sigma^2 (\mathbb X^T \mathbb X)^{-1} =
\sigma^2 \mathbb D \mathbb D^T
$$
Matice A je [[Matice - Pozitivně semidefinitní]]. Rozptyl obecného odhadu je tedy vždy větší nebo roven odhadu pomocí OLS.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
