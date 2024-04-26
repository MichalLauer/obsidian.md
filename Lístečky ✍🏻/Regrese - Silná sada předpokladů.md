---
Datum: 2024-03-21
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese/MLR 
# Regrese - Silná sada předpokladů
Silná sada předpokladů rozšiřuje [[Regrese - Slabá sada předpokladů|slabou sadu předpokladů]] o to, že chyby modelu jsou [[iid]].
$$
\epsilon \sim NID(0, \sigma^2)
$$
Jednotlivé předpoklady jsou pak upravené.
## Předpoklady
1) **Vektor střední hodnot** chybové složky je 0
$$
E(\epsilon) = \mathbb 0
$$
2) **Kovarianční matice** chybové složky má na diagonále stejný rozptyl; mimo je nulová
$$
C(\epsilon) = \sigma^2 \mathbb I
$$
3) Z předpokladů vyplívá, že chyby mají **Vícerozměrné normální rozdělení**
$$
\epsilon \sim N(\mathbb 0, \sigma^2 \mathbb I)
$$
## Implikace
Díky tomuto předpokladu víme i rozdělení pro vyrovnané hodnoty.
$$
\begin{align}
E(\mathbb y) &= \mathbb\beta \mathbb X \\
C(\mathbb y) &= \sigma^2 \mathbb I\\
\mathbb y &\sim N(\mathbb\beta \mathbb X, \sigma^2 \mathbb I)
\end{align}
$$
Také je odvozeno rozdělení pro jednotlivé složky regresního modelu.
$$
\begin{align}
b &\sim N(\beta, \sigma^2(\mathbb X^T \mathbb X)^{-1}) \\
\hat y &\sim N(\mathbb X \mathbb\beta, \sigma^2 \mathbb H) \\
e &\sim N(\mathbb 0, \sigma^2 \mathbb M) \\
x_*^T b &\sim N(\mathbb x_*^T \mathbb\beta, \sigma^2 x_*^T (\mathbb X^T \mathbb X)^{-1} x_*) \\
y_* - \hat y_* = y_* - \mathbb x_*^T \mathbb b &\sim N(0, \sigma^2 (1 + x_*^T (\mathbb X^T \mathbb X)^{-1} x_*)) \\
\frac{(n - p) s^2(e)}{\sigma^2} &\sim \chi^2(n - p)
\end{align}
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
