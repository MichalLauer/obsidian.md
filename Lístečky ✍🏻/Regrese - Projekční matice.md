---
Datum: 2024-02-27
Typ:
  - Permanentní
aliases:
- Hat matice
- Matice H
---
*Klíčová slova:* #Regrese/MLR
# Regrese - Projekční matice
Matice vychází z [[Optimalizace - Metoda nejmenších čtverců|metody nejmenších čtverců]]
$$
\mathbb{H} = 
\mathbb{X}\mathbb{\beta} =
\mathbb{X}\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T
$$
Matice je [[Matice - Symetričnost|symetrická]] a [[Matice - Idempotentní|idempotentní]]. Díky kombinaci těchto dvou vlastností lze zapsat každý **prvek na diagonále** matice jako
$$
h_{ii} = \sum_j h_{ij}h_{ji} = \sum_j h_{ij}^2 \implies 0 \leq h_{ii} \leq 1.
$$
[[Matice - Stopa]] lze odvodit jako
$$
\text{st}(\mathbb{H}) =
\text{st}(\mathbb{X}\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T) =
\text{st}(\mathbb{I}) = p.
$$
Průměrná hodnota diagonální hodnoty je tedy $p/n$.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
