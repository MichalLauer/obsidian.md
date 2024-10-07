---
Datum: 2024-09-20
Typ:
  - Permanentní
aliases:
  - Čebyševovou nerovností I. typu
---
*Klíčová slova:* #Pravděpodobnost 
# Markovova nerovnost
[[Robustní statistika]] odhad horní hranice pravděpodobnosti, že náhodná veličina překročí hranici $a > 0$. Platí u **obecné nezáporné náhodné** veličiny $X$ s konečným průměrem.
$$
P(X \geq a) \leq \frac{E(X)}{a}
$$
## Odvození
Klasický [[Střední hodnota]] lze rozepsat jako součin dvou podmíněných.
$$
E(X) = E(X|X \geq a)p(X \geq a) + E(X|X < a)p(X < a)
$$

Jelikož oba výrazy budou vždy kladné ($X > 0, a > 0$), pak platí
$$
E(X) \geq E(X \geq a)p(X \geq a)
$$
Dále platí, že $E(X \geq a) \geq a$ a díky tomu lze výraz substituovat, čímže se nerovnice oslabí ale stále je platná.
$$
E(X) \geq aP(X \geq a) \implies P(X \geq a) \leq \frac{E(X)}{a}
$$
# Známé minimum
Mějme speciální případ, kdy **nezáporná náhodná veličina** $X > c > 0$. Známe tedy minimum náhodné veličiny $X$. Pro nalezení horní hranice pravděpodobnosti, že $X$ překročí hranici $a > c$, lze reparametrizovat Markovovu nerovnost jako
$$
Y = X - c, b = a - c,
$$
a díky tomu
$$
\begin{align}
P(Y \geq b) &\leq \frac{E(Y)}{b} \\
P(X - c \geq a - c) &\leq \frac{E(X - c)}{a - c} \\
P(X \geq a) &\leq \frac{E(X) - c}{a - c}.
\end{align}
$$
Upravená hranice je vždy menší než původní hranice $E(X) / a$, neboť
$$
\begin{align}
a &\geq E(X) \\
ca &\geq cE(X) \\
aE(X) + ca &\geq aE(X) + cE(X)  \\
aE(X) - cE(X) &\geq aE(X) -ac \\
E(X)(a - c) &\geq a(E(X) - c) \\
\frac{E(X)}{a} &\geq \frac{E(X) - c}{a - c}.
\end{align}
$$
> [!NOTE] Autor
> Tohle vymyslel p. Štěpánek a ještě to nepublikoval - NEOKOPÍROVAT!!!