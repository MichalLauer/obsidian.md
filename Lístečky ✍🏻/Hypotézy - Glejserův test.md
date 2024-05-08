---
Datum: 2024-05-08
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Hypotézy/Rozptyl 
# Hypotézy - Glejserův test
Testujeme, zda má rozptyl určitý monotónní tvar.
$$
\begin{align}
\text{H0}&: \sigma^2_1 = \sigma^2_2 = \dots = \sigma^2_k \\
\text{H1}&: \sigma^2 = ax + b
\end{align}
$$
Používá se primárně u regresních modelů a testování rozptylu.
## Postup
U doplňkové regrese se k vysvětlení použijí absolutní hodnoty původních residuí. K nim se pak přidají různé matematické transformace původních vysvětlujících proměnných (nebo pouze proměnné). Pokud je některý koeficient významný, zamítáme h0.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]