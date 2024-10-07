---
Datum: 2024-06-15
Typ:
  - Permanentní
aliases:
  - Law of total probability
---
*Klíčová slova:* #Pravděpodobnost
# Pravděpodobnost - Celková pravděpodobnost
Věta říká, že pravděpodobnost jevu $A$ lze vyjádřit jako součet pravděpodobnosti jevu $A$ podmíněný všemi stavy jevu $B$.
$$
P(A)=\sum_{i=1}^n P(A|B_i)P(B_i)
$$
To samé lze vyjádřit pomocí [[Pravděpodobnost - Součin pravděpodobností|součinu]] jevu $A$ a jednotlivých stavů $B_i$.
$$
P(A)=\sum_{i=1}^k P(A \cap B_i)
$$
## Předpoklady
Podstatné je to, že jev $B$ lze vyjádřit pomocí diskrétních jevů $1, 2, \dots, n$, které jsou vyčerpávající a navzájem exkluzivní.
