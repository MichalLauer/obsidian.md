---
Datum: 2024-04-21
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Generování
# Generování - Metropolis-Hastings algoritmus
Algoritmus slouží k simulaci náhodných hodnot z [[Pravděpodobnostní rozdělení]] $p(x)$. Řadí se do algoritmů typu [[Optimalizace - Markov chain Monte Carlo|Optimalizace - MCMC]].
# Generování
Pro generování nové hodnoty $x_{n+1}$ pomocí $x_n$ je nutné určit **kandidáta** $x^*$. Po vygenerování kandidáta z **navrhovaného rozdělení** je nutné vygenerovat **zamítací hranici** $A(x^*, x_n)$. Vygenerovaná hodnota je s pravděpodobnostní $A(x^*, x_n)$ přijata a $1 - A(x^*, x_n)$ zamítnuta.
$$
x_{n+1} =
\begin{cases}
x^*  &\text{ s prav. } A(x^*, x_n) \\
x_n &\text{ s prav. } 1 - A(x^*, x_n) \end{cases}
$$
Důležité je zvolit vhodný počáteční bod $x_0$, jinak je několik prvních hodnot zkreslených a je nutné použít **burning**. Zvolením nevhodného navrhovaného rozdělení (resp. jeho parametrů) také mohou být generované hodnoty vysoce korelované a je potřeba použít **lag**.
## Navrhované rozdělení
Navrhované rozdělení musí být závislé pouze na aktuálně vygenerované hodnotě $x_n$ (*proto Markov Chain*).
$$
x_* \sim g(x | x_n)
$$
Teoreticky může být libovolné, ale často se volí 
$$
x_* \sim N(x_n, \sigma^2)
$$
## Hranice zamítnutí
Hranice je dána podílem
$$
A(x^*, x_n) = \frac{p(x^*)}{p(x_n)} \frac{g(x_n | x^*)}{g(x^* | x_n)}.
$$
Hodnota $p(\cdot)$ značí pravděpodobnost (hustotu) z rozdělení, ze kterého chceme získat generované hodnoty. $g(\cdot)$ pak značí pravděpodobnost (hustotu) z rozdělení, které je zvoleno jako navrhované.
### Intuice
První poměr (pouze $p$) označuje to, jestli je kandidát více pravděpodobný než aktuální hodnota. Pokud je zlomek $> 1$, hustota $p(x^*) > p(x_n)$ a je tedy více pravděpodobné, že se tam algoritmus chce dále posunout.
## Burning
Pokud je hodnota $x_0$  *mimo* požadované rozdělení, prvních několik generovaných hodnot může výsledek zkreslovat. Proto se často několik prvních hodnot zahodí.
## Lag
V případě, že je navrhované rozdělení hodně široké, generované hodnoty se budou *pohybovat* velmi pomalu a vzniká mezi nimi autokorelace. Toto může nastat např. vysokým rozptylem v normální rozdělení. Pokud taková situace nastane, je vhodné z generovaných hodnot do finální sady čísel vzít každé $l$-lté pozorování.

- - -
# Literatura
https://blog.djnavarro.net/posts/2023-04-12_metropolis-hastings/
https://www.youtube.com/watch?v=yCv2N7wGDCw