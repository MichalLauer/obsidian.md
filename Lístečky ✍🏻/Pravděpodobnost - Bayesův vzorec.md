---
Datum: 2024-06-15
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Pravděpodobnost
# Pravděpodobnost - Bayesův vzorec
Vzorec vyjadřuje pravděpodobnost jevu $A$ za předpoklady, že se stal jev $B$.
$$
P(A|B)=\frac{P(B|A)P(A)}{P(B)}
$$
Lze vyjádřit z případu, kdy je se počítá [[Pravděpodobnost - Součin pravděpodobností|součin]] dvou **závislých** pravděpodobností.
$$
P(A)P(B|A)=P(B)P(A|B) \implies P(A|B)=\frac{P(B|A)P(A)}{P(B)}
$$
Často se používá i vyjádření pomocí [[Pravděpodobnost - Celková pravděpodobnost|celkové pravděpodobnosti]].
$$
P(A|B)=\frac{P(B|A)P(A)}{\sum_{i=1}^n P(B|A_i)P(A_i)}
$$

