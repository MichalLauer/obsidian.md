---
Datum: 2024-03-21
Typ:
  - Bibliografická
aliases:
 - Regrese - Klasické předpoklady
---
*Klíčová slova:* #Regrese/MLR 
# Regrese - Silná sada předpokladů
Silná sada předpokladů rozšiřuje [[Regrese - Slabá sada předpokladů|slabou sadu předpokladů]] o to, že chyby modelu jsou [[iid]] a mají [[Normální rozdělení]]
$$
\begin{align}
\epsilon_i &\sim NID(0, \sigma^2) \\
\epsilon   &\sim N(\mathbb 0, \sigma^2 \mathbb I)
\end{align}
$$
Jednotlivé předpoklady jsou pak upravené. 
## Implikace
Pokud platí silná sada, automaticky to implikuje [[Regrese - Gauss-Markův teorém]]. Dále také víme:
$$
\begin{align}
E(\mathbb y) &= E(\mathbb\beta \mathbb X + \epsilon) = \mathbb\beta \mathbb X \\
C(\mathbb y) &= C(\mathbb \epsilon) = \sigma^2 \mathbb I\\
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
