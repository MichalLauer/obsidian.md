---
Datum: 2024-04-21
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Generování
# Generování - Metropolisův algoritmus
Speciální případ [[Generování - Metropolis-Hastings algoritmus]] algoritmu, ve kterém je **navrhované rozdělení symetrické**. Díky tomu se **hranice zamítnutí** vypočítá pouze jako
$$
A(x^*, x_n) = \frac{p(x^*)}{p(x_n)}.
$$
Ostatní postup zůstává identický.
## Vykrácení
Pokud je rozdělení symetrické, poté se
$$
g(x_n | x^*) = g(x^* | x_n)
$$
kvůli tomu, že v symetrickém rozdělení je vzdálenost mezi $E(\cdot)$ a $x_n$, resp. $x^*$ stejná.
- - -
# Literatura
https://blog.djnavarro.net/posts/2023-04-12_metropolis-hastings/

