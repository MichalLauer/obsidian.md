---
Datum: 2024-03-10
Typ:
  - Bibliografická
aliases:
  - Regrese - predikované hodnoty
---
*Klíčová slova:* #Regrese/MLR 
# Regrese - Vyrovnané hodnoty
Vyrovnané, též predikované, hodnoty jsou výsledek lineární transformace nezávislých proměnných.
$$
\mathbb{\hat{y}} = \mathbb{X}\mathbb{\hat\beta} = \mathbb{H}\mathbb{y}
$$
Pokud je splněn předpoklad o [[Regrese - Nezávislost residuí|nezávislosti residuí]], **očekávaná hodnota** vyrovnané hodnoty je samotná lineární transformace.
$$
E(\mathbb{y}) = E(\mathbb{X}\mathbb{\hat\beta}) =
\mathbb{X}E(\mathbb{\hat\beta}) = \mathbb{X}\mathbb{\beta}
$$
**Kovarianční matice** predikovaných hodnot je za platnosti [[xRegrese - Homoskedasticita|homoskedasticity]] analyticky definována jako
$$
C(\mathbb{\hat{y}}) = C(\mathbb{X}\mathbb{\hat\beta}) =
\mathbb{X}C(\mathbb{\hat\beta})\mathbb{X}^T =
\mathbb{X}\sigma^2\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T =
\sigma^2 \mathbb{H}.
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]