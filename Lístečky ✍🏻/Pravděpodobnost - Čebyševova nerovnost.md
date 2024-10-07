---
Datum: 2024-09-20
Typ:
  - Permanentní
aliases:
  - Čebyševovou nerovností II. typu
---
*Klíčová slova:* #Pravděpodobnost
# Čebyševova nerovnost
[[Robustní statistika]] odhad spodní hranice pravděpodobnosti, že se náhodná veličina $X$ s konečnou $E(X)$ a $D(X)$ absolutně vzdálí od střední hodnoty maximálně o konstantu $a >0$.
$$
\begin{align}
P\left(|X - E(X)| \leq \epsilon\right)
  &\geq \frac{D(X)}{\epsilon^2} \\
P\left(|X - E(X)| \leq \epsilon\sqrt{D(X)}\right)
  &\geq \frac{1}{\epsilon^2}
\end{align}
$$
## Odvození
Pro odvození je nutné použít [[Pravděpodobnost - Markovova nerovnost]] a parametrizovat jako
$$
X = (Y - E(Y))^2, a = \epsilon^2.
$$
Po dosazení lze získat
$$
\begin{align}
P(X \geq a) &\leq \frac{E(X)}{a} \\
P((Y - E(Y))^2 \leq \epsilon^2)
  &\leq \frac{E((Y - E(Y))^2)}{\epsilon^2} \\
P\left( |Y - E(Y)| \leq \epsilon\right) &\leq \frac{D(Y)}{\epsilon^2},
\end{align}
$$
resp. pokud $a = \epsilon^2D(Y)$
$$
\begin{align}
P(X \geq a) &\leq \frac{E(X)}{a} \\
P((Y - E(Y))^2 \leq \epsilon^2D(X))
  &\leq \frac{E((Y - E(Y))^2)}{\epsilon^2D(Y)} \\
P\left( |Y - E(Y)| \leq \epsilon\sqrt{D(Y)}\right)
  &\leq \frac{1}{\epsilon^2},
\end{align}
$$