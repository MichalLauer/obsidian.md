---
Datum: 2024-02-27
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Optimalizace 
# Optimalizace - Konvexní funkce
Konvexní funkce znamená, že lokální minimum funkce je zároveň její globální minimum. Matematicky lze zapsat jako
$$
f(\lambda x_1 + (1 - \lambda)x_2) \leq \lambda f(x_1) + (1 - \lambda)f(x_2)
$$
pro libovolná $x_1, x_2$ z intervalu $\langle a, b \rangle$ a $\lambda \in (0, 1)$.
Pokud existují derivace funkce $f(x)$ na intervalu $\langle a, b \rangle$, poté postačující podmínka pro konvexnost je ta, že $f''(x) \geq 0$ pro všechna $x \in \langle a, b \rangle$.

> [!warning] Konkávní funkce
> V některé literatuře se může psát o konkávních funkcích. Tyto funkce však neexistují, nedávají smysl, a pouze se jedná o $-f(x)$, reps. hledání maxim.

- - -
# Literatura
[[Sokol2023_4EK632OptimalizacniModely|SOKOL, Ondřej, 2023. 4EK632 Optimalizační modely (v angličtině). In: . Prague University of Economics and Business.]]
