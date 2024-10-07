---
Datum: 2024-06-01
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Variační inflační faktor
Ukazatel, pomocí kterého lze měřit, jak moc je ovlivněn rozptyl [[Regrese - Metoda nejmenších čtverců|odhadnutého koeficientu]] kvůli problému [[Regrese - Předpoklad plné hodnosti]]. Rozptyl koeficientu $b_j$ lze vyjádřit jako 
$$
s(b_j) = \sqrt{
\frac{s^2(e)}{(n-1)s_j^2} \times \frac{1}{1 - I_j^2}.
}
$$
Ve vzorečku je důležitý právě druhý zlomek, kde $I_j^2$ představuje [[Koeficient determinace|Index determinace]] v regresním modelu, kde predikujeme proměnnou $j$ podle všech ostatních proměnných. Tento výraz se právě nazývá **Variační inflační faktor (VIF)**.
- - -
# # Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]