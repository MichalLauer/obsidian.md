---
Datum: 2024-04-18
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese 
# Regrese - Přínos jednotlivých proměnných
V [[Regrese|regresi]] lze vypočítat přínos jednotlivých proměnných $X_1, \dots, X_k$ k celkovému [[Součet vysvětlených čtverců|regresnímu součtu čtverců]]. Díky součtu residuím lze vyjádřit $b_0$ jako
$$
\begin{align}
\sum_{i=1}^n e_i &= 0 \\
\sum_{i=1}^n (y_i - (b_0 + b_1x_{i,1} + \dots + b_kx_{i,k})) &= 0 \\
\overline y - b_0 - b_1 \overline x_1 - \dots - b_k \overline x_k &= 0 \\
\overline y - b_1 \overline x_1 - \dots - b_k \overline x_k &= b_0.
\end{align}
$$
To lze dosadit do klasického regresního modelu a získáváme
$$
\begin{align}
\hat y_i &= (\overline y - b_1 \overline x_1 - \dots - b_k \overline x_k) + b_1 x_{i,1} + \dots + \beta_k x_{i, k} \\
\hat y_i &= \overline y + b_1 (x_{i,1} - \overline x_1) + \dots + b_k (x_{i, k} -\overline x_k) \\
(\hat y_i - \overline y) &=  b_1 (x_{i,1} - \overline x_1) + \dots + b_k (x_{i, k} -\overline x_k) \\
(\hat y_i - \overline y) &=  b_1 (x_{i,1} - \overline x_1) + \dots + b_k (x_{i, k} -\overline x_k) \\
Q(\hat y_i) &=  b_1 Q(x_1, \hat y) + \dots + b_k Q(x_k, \hat y).
\end{align}
$$
A tedy [[Součet vysvětlených čtverců|Regresní součet čtverců]] je vyjádřen pomocí jednotlivých odhadnutých koeficientů a párových regresních součtů. Vztah lze jednoduše převést i na rozložení [[Koeficient determinace|koeficientu determinace]] pomocí [[Parciální koeficient determinace]].
$$
\begin{align}
Q(\hat y_i) &=  b_1 Q(x_{i,1}, \hat y) + \dots + b_k Q(x_{i, k}, \hat y) \\
R^2 &=  b_1 r^2(x_1, \hat y) + \dots + b_k r^2(x_k, \hat y)
\end{align}
$$

> [!warning] Praktičnost
> Tento rozklad není moc používaný, protože se může stát, že je přínos záporný (v případě, že se znaménko $b_j$ nerovná $Q(x_j, \hat y)$). Náhradou může být [[Regrese - Postupný rozklad regresního součtu čtverců]].

- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
