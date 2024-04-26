---
Datum: 2023-12-28
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Regrese 
# Elasticita regresních koeficientů
Při [[Regrese|regresi]] lze různými způsoby měřit elasticitu a vliv závislých proměnných na nezávislou proměnnou, [[Ceteris Paribus]]. Tabulka níže sumarizuje vztahy a jejich interpretace (Wooldridge 2020, s. 39).

| # | Model | Změna |
| ---- | ---- | ---- |
| 1) | level - level | $\Delta y = \beta_1 \Delta x$ |
| 2) | level - log | $\Delta y = (\beta_1/100)\% \Delta x$ |
| 3) | log - level | \%$\Delta y \approx (100\beta_1) \Delta x$ |
| 4) | log - log | $\% \Delta y = \beta_1 \% \Delta x$ |
## 1) Level - Level
$$y = \beta_0 + \beta_1x$$
Zde se interpretuje pouze jednotková změna, tedy **jednotková změna $x$ vede ke změně v $y$ o velikosti $\beta_1$**, [[Ceteris Paribus]].
## 2) Level - Log
$$y = \beta_0 + \beta_1\log(x)$$
V tomto případě **jednoprocentní změna $x$ vede k $(\beta_1/100)$ změně v $y$**, [[Ceteris Paribus]].
## 3) Log - Level (semi-elasticita)
$$\log(y) = \beta_0 + \beta_1 x$$
Pokud je logaritmovaná nezávislá proměnná, interpretuje se změna tak, že **jednotková změna v $x$ vede k $100*\beta_1$ procentní změně v $y$**, [[Ceteris Paribus]].

> [!NOTE] Aproximativní změna
> Slouží pouze jako aproximace u malých $\beta$. Pro exaktní změnu je nutné koeficient exponovat, tedy $\% \Delta y = 100[\exp(\beta_1) - 1] \Delta x$ (Zouhar 2023, přednáška 5)
## 4) Log - Log (elasticita)
$$\log(y) = \beta_0 + \beta_1 \log(x)$$
Kombinace obou log transformací označuje elasticitu, kde **jednoprocentní změna $x$ vede k $\beta_1$ procentní změně v $y$**, [[Ceteris Paribus]].

- - -
# Literatura
[[Zouhar2023_4EK333Ekonometrie|ZOUHAR, Jan, 2023. 4EK333 Ekonometrie 1. In: . Prague University of Economics and Business.]]
[[Wooldridge2020_IntroductoryEconometricsModern|WOOLDRIDGE, Jeffrey M., 2020. Introductory econometrics: a modern approach. Seventh edition. Boston, MA: Cengage. ISBN 978-1-337-55886-0.]]
