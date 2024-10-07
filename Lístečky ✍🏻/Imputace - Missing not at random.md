---
Datum: 2024-09-29
Typ:
  - Bibliografická
aliases:
  - MNAR
---
*Klíčová slova:* #Imputace 
# Imputace - Missing not at random
Data chybí kvůli datům samotným. Může se jednat o pacienty, kteří nenahlásí vysokou teplotu právě kvůli tomu, že teplota samotná je vysoká.
## Dvoustupňová regrese
Vhodným řešením je dvoustupňová regrese. Pokud proměnná $x$ obsahuje chybějící hodnoty MNAR a proměnné $z$ jsou kompletní, pak lze modelovat
$$
P(X \text{ chybí}) = p = z \hat \beta
$$
Výsledné pravděpodobnosti $p$ lze zařadil do hlavního modelu místo proměnné $x$.
- - -
# Literatura
[[Formanek2024_4EK417PraktikumEkonometrie|FORMÁNEK, Tomáš, 2024. 4EK417 Praktikum z ekonometrie. In: . Prague University of Economics and Business.]]