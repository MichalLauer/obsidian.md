---
Datum: 2024-06-01
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Inference
Inference se liší podle toho, jaké máme splněné předpoklady. U regrese můžeme nejčastěji testovat
- [[Regrese - Testování koeficientů]]
- [[Regrese - Testování střední hodnoty predikce]]
- [[Regrese - Testování predikce]]
## [[Regrese - Silná sada předpokladů]]
V tomto případě mají residua normální rozdělení a testování hypotéz je validní pro jakékoliv $n$.
$$
T \sim T(\dots)
$$
## [[Regrese - Gauss-Markův teorém]]
Pokud data splňují teorém ale residua nemají vícerozměrné normální rozdělení, inferenci lze stále provést, ale spoléháme u toho na [[CLT]].
$$
T \overset{D}{\sim} T(\dots)
$$
## Známý rozptyl residuí
V případě, že nemusíme odhadovat rozptyl residuí a z nějakého (teoretického) důvodu ho známe, je možné použít normální rozdělení. Tento rozdíl je s velkým $n$ malý.
$$
T \sim N(0, 1)
$$
- - -
# Literatura

