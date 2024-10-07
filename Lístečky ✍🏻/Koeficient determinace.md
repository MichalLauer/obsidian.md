---
Datum: 2023-12-27
Typ:
  - Bibliografická
aliases:
 - Index determinace
---
*Klíčová slova:* #Metrika
# Koeficient determinace
Koeficient určuje, kolik % rozptylu je vysvětleno z celkového rozptylu (Wooldridge 2020, s. 35). K výpočtu se primárně používá [[Součet vysvětlených čtverců|SSE]] a [[Celkový součet čtverců|SST]].
$$
R^2 = \frac{\text{SSE}}{\text{SST}} = 1 - \frac{\text{SSR}}{\text{SST}}
$$
Hodnoty se pohybují na intervalu $\langle0, 1\rangle$. S přidáním dalších vysvětlujících proměnných koeficient [[Regrese - Změny součtů čtverců|nemůže být nikdy menší]], proto ho není vhodné používat pro porovnání různých modelů. Při použití [[Regrese - Metoda nejmenších čtverců]] se $R^2$ [[Regrese - Změny součtů čtverců|maximalizuje]].

> [!DANGER] Různé interpretace
> Ne u každé regrese či metody má koeficient stejný význam a stejný obor hodnot.

- - -
# Literatura
[[Wooldridge2020_IntroductoryEconometricsModern|WOOLDRIDGE, Jeffrey M., 2020. Introductory econometrics: a modern approach. Seventh edition. Boston, MA: Cengage. ISBN 978-1-337-55886-0.]]