---
Datum: 2024-02-27
Typ:
  - Permanentní
aliases: Matice residuí
---
*Klíčová slova:* #Regrese 
# Regrese - Matice M
Matice residuí má tvar $\mathbb{M} = \mathbb{I} - \mathbb{H}$, kde matice $\mathbb{H}$ značí [[Regrese - Projekční matice|projekční matici]]. Lze odvodit jako
$$
\begin{align}
\mathbb{e}
&= \mathbb{y}-\hat{\mathbb{y}} \\
&= \mathbb{y} - \mathbb{H}\mathbb{y} \\
&= \left(\mathbb{I}-\mathbb{H}\right)\mathbb{y} \\
&= \mathbb{M}\left(\mathbb{X}\mathbb{\beta} + \mathbb{\epsilon} \right) \\
&= \mathbb{M} \mathbb{\epsilon}.
\end{align}
$$
A tedy rovná se $\mathbb{M} = \mathbb{I} - \mathbb{H}$.
Matice je [[Matice - Symetričnost|symetrická]] a [[Matice - Idempotentní|idempotentní]].

- -  -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]