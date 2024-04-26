---
Datum: 2024-03-10
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese/MLR 
# Regrese - Predikované hodnoty
Pokud se používá nová kombinace proměnných $\mathbb{x}_*$, pak lze odhad zapsat jako
$$
y_* = \eta_* + \epsilon_* = \mathbb{x}_*^T\beta + \epsilon_*
$$
Odhad střední hodnoty lze zapsat jako
$$
\mathbb{\hat\eta}_*= \mathbb{x}_*^T\mathbb{\hat\beta}.
$$
**Očekávaná hodnota** střední hodnoty je
$$
E(\hat\eta_*) = E(\mathbb{x}_*^T\hat\beta) = \mathbb{x}_*^T\beta,
$$
a **rozptyl** je dán
$$
D(\hat\eta_*) = \mathbb x^T_* C(\hat\beta) \mathbb x_*
= \sigma^2 \mathbb x^T_* (\mathbb{X}^T\mathbb{X})^{-1} \mathbb x_,
$$
a je **odhadnut** pomocí
$$
s^2(\hat\eta_*) =  s^2(e) \mathbb x^T_* (\mathbb{X}^T\mathbb{X})^{-1} \mathbb x_.
$$
# Chyba odhadu
Celkový chyba predikce je dána
$$
y_* - \hat{y}_* = \mathbb{x}_*^T\beta + \epsilon_* - \mathbb{x}_*^T\hat\beta =
\mathbb{x}(\beta - \hat\beta) + \epsilon_*
$$
**Střední hodnota** chyby je
$$
E(y_* - \hat{y}_*) = 0
$$
a **rozptyl** chyby je dán
$$
\begin{align}
D(y_* - \hat{y}_*) &= D(\mathbb{x}(\beta - \hat\beta) + \epsilon_*) \\
&= D(\mathbb{x}\hat\beta) + D(\epsilon_*) \\
&= \sigma^2 \mathbb x^T_* (\mathbb{X}^T\mathbb{X})^{-1} \mathbb x_* + \sigma^2 \\
&= \sigma^2(1 + \mathbb x^T_* (1 + \mathbb{X}^T\mathbb{X})^{-1} \mathbb x_*).
\end{align}
$$
**Odhad rozptylu** je poté
$$
s^2(y_* - \hat{y}_*) = s^2(e) (1 + \mathbb x^T_* (\mathbb{X}^T\mathbb{X})^{-1} \mathbb x_*).
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]