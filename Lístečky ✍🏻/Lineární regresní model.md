---
Datum: 2023-12-28
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Regrese
# Lineární regresní model
Modely, které popisují **lineární vztah mezi predikovanou hodnotou a prediktory**. Linearita platí pro jednotlivé koeficienty, proto transformace jako $\log(x), x^2, 100x, \sqrt{x} \dots$ jsou v pořádku. Naproti tomu model
$$
y = \beta_0 + \beta_1x^{\beta_2}
$$
už v parametrech lineární není, a proto by se nejednalo o lineární model (Wooldridge 2020, s. 40).
V populaci se bavíme o teoretické [[Regrese - Populační regresní funkce]] a [[Regrese - Populační regresní model]], které jsou odhadnuty pomocí [[Regrese - Výběrová regresní funkce]], [[Regrese - Výběrový regresní model]] a nasbíraných dat. Funkce popisuje očekávanou (průměrnou) hodnotu vysvětlované proměnné, zatímco model se soustředí na jednotlivá pozorování (Zouhar 2023, s. 3 přednáška 2).
## Koeficienty
Pomocí koeficientů lze měřit [[Elasticita regresních koeficientů|elasticita]]. Lineární transformace veličin ($x*100$) pak způsobují úměrnou změnu v parametrech (Wooldridge 2020, s. 39).
# Typy modelů
Mezi základní typy patří:
- [[xSLR - Jednoduchý regresní model]]
- - -
# Literatura
[[Wooldridge2020_IntroductoryEconometricsModern|WOOLDRIDGE, Jeffrey M., 2020. Introductory econometrics: a modern approach. Seventh edition. Boston, MA: Cengage. ISBN 978-1-337-55886-0.]]
[[Zouhar2023_4EK333Ekonometrie|ZOUHAR, Jan, 2023. 4EK333 Ekonometrie 1. In: . Prague University of Economics and Business.]]
