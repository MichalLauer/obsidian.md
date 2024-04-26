---
Datum: 2024-03-21
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:*  #Regrese/MLR 
# Regrese - Podmínkový odhad
Na regresní koeficienty lze klást podmínky ve formě
$$
\mathbb R \mathbb \beta = r.
$$
## Příklad
Podmínku $\beta_1 = \beta_2 = 0$ lze zapsat jako
$$
\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
\beta_1 \\
\beta_1 \\
\beta_2
\end{bmatrix}
=
\begin{bmatrix}
0 \\
0
\end{bmatrix}.
$$
Podmínku $\beta_1 + \beta_2 = 1$ lze zapsat jako
$$
\begin{bmatrix}
0 & 1 & 1
\end{bmatrix}
\begin{bmatrix}
\beta_0 \\
\beta_1 \\
\beta_2
\end{bmatrix}
=
1.
$$
Podmínku $\beta_1 = \beta_2$ lze zapsat jako
$$
\begin{bmatrix}
0 & 1 & -1 \\
1 & 0 & 0
\end{bmatrix}
\begin{bmatrix}
\beta_0 \\
\beta_1 \\
\beta_2
\end{bmatrix}
=
\begin{bmatrix}
0 \\
0
\end{bmatrix}.
$$
## Výpočet
Po použití [[Metoda Lagrangeových multiplikátorů]] lze nové odhady zapsat jako
$$
b_p = b - (\mathbb X^T \mathbb X)^{-1}R^TK^{-1}(R b-r),
$$
kde $K = R(\mathbb X^T \mathbb X)^{-1} R^T$ a $b$ je klasický odhad pomocí [[Regrese - Metoda nejmenších čtverců]].
## Vlastnosti
**Očekávaná hodnota** regresních koeficientů je zkreslená.
$$
E(b_p) = \beta - (\mathbb X^T \mathbb X)^{-1}R^TK^{-1}(R b-r)
$$
V případě, že odhadnuté koeficienty už podmínky splňují ($Rb = r$), odhad je nezkreslený.
**Kovarianční matice** regresních koeficientů je
$$
C(b_p) = \sigma^2 \left(
(\mathbb X^T \mathbb X)^{-1} - (\mathbb X^T \mathbb X)^{-1}
R^TK^{-1} R (\mathbb X^T \mathbb X)^{-1}
\right).
$$
**Součet residuí** bude vždy (pokud $Rb \neq r$) větší než z metody nejmenších čtverců.
$$
Q(e_P) = Q(e) + (Rb - r)^T K^{-1} (Rb - r)
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
