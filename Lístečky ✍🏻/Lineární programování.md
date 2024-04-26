---
Datum: 2024-02-28
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Optimalizace/LineárníProgramování 
# Lineární programování
Lineární programování slouží k optimalizaci funkce, která lze zapsat jako lineární vztah
$$
c_1x_1 + c_2x_2 + \dots + c_nx_n \rightarrow \max,
$$
pomocí vektorů také jako
$$
c^Tx \rightarrow \max.
$$
## Podmínky
Tato funkce musí splňovat podmínky, které jsou znovu definované lineárním vztahem
$$
\begin{align}
2x_1 + 3x_2 \leq 5 \\
8x \leq 3.
\end{align}
$$
Matematicky lze rozepsat podmínky do matice strukturálních změn $\mathbb{A}$ a vektoru $b$.
$$
\mathbb{A} = 
\begin{bmatrix}
2 & 3 \\
1 & 0
\end{bmatrix}; \space
x = 
\begin{bmatrix}
x_1 \\
x_2 
\end{bmatrix}; \space
b = 
\begin{bmatrix}
5 \\
3 
\end{bmatrix},
$$
neboli
$$
\mathbb{A}x \leq b.
$$
Většinou se implicitně uvažují kladná $x$, tedy
$$
x_i \geq 0; i = 1, \dots, n.
$$
- - -
# Literatura
[[Sokol2023_4EK632OptimalizacniModely|SOKOL, Ondřej, 2023. 4EK632 Optimalizační modely (v angličtině). In: . Prague University of Economics and Business.]]