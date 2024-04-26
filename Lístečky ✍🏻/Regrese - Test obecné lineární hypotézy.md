---
Datum: 2024-03-23
Typ:
  - Bibliografická
aliases:
  - Regrese - F-test
---
*Klíčová slova:* #Regrese
# Regrese - Test obecné lineární hypotézy
Pomocí testu lze porovnat významnost [[Regrese - Podmínkový odhad|podmínkového odhadu]].
$$
\begin{align}
H_0&: R\beta = R \\
H_1&: R\beta \neq R
\end{align}
$$
To lze udělat díky propojení dvou [[Chí-kvadrát rozdělení]]. První popisuje rozdělení rozdílu čtvercových součtu residuí.
$$
\frac{Q(e_P) - Q(e)}{\sigma^2} \sim \chi^2(J)
$$
Druhé pak rozdělení čtvercového součtu residuí u odhadu pomocí [[Regrese - Metoda nejmenších čtverců|metodou nejmenších čtverců]].
$$
\frac{Q(e)}{\sigma^2} \sim \chi^2(n - p)
$$
Rozdělení lze spojit do [[F rozdělení]].
$$
F = \frac{\frac{Q(e_P) - Q(e)}{J\sigma^2}}{\frac{Q(e)}{(n-p)\sigma^2}} =
\frac{\frac{Q(e_P) - Q(e)}{J}}{\frac{Q(e)}{(n-p)}} \sim F(J, n-p)
$$
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
