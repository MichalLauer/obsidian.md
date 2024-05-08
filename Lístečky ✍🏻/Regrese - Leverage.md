---
Datum: 2024-03-10
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Leverage
Hodnoty leverage lze v regresi získat z [[Regrese - Projekční matice|Matice H]], resp. z jejich diagonálních hodnot. Jelikož víme, že každá hodnota $h_{ii}$ je v průměru $p / n$, hodnoty extrémně odlišné mohou naznačovat to, že dané pozorování má na regresi významný vliv.
## Vliv počtu pozorování a proměnných
Hodnota leverage se se zvyšujícím se počtem regresorů (nezávislých proměnných) neklesne, *hodnoty jsou tedy pro pevné n neklesající funkcí počtu regresorů*.
Pokud jsou však pro pevné p přidávána další pozorování, hodnota leverage neporoste. *Pro pevné p je tedy hodnota leverage nerostoucí funkcí n*.
## Vztah k [[Mahalanobisova vzdálenost]]
Leverage jednotlivých pozorování lze vyjádřit jako
$$
h_{ii} = \frac{1}{n} + \frac{1}{n - 1} \Delta_i^2.
$$
Ve vzdálenosti je použit centroid a kovarianční matice z datové matice.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
https://stats.stackexchange.com/questions/199686/prove-the-relation-between-mahalanobis-distance-and-leverage/200566#200566
