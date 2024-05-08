---
Datum: 2024-04-20
Typ:
  - Bibliografická
aliases:
 - Regrese - nestoupající SSR
 - Regrese - neklesající SSE
---
*Klíčová slova:* #Regrese 
# Regrese - Změny součtů čtverců
Pokud do [[Vícerozměrný regresní model]] přidáme *jakoukoliv* další vysvětlující proměnnou, [[Součet vysvětlených čtverců|SSE]] se může pouze zvýšit a [[Součet čtverců reziduí|SSR]] se může pouze snížit. Jelikož [[Celkový součet čtverců|SST]] není ovlivněno počtem vysvětlovaných proměnných (*zůstává konstantní*), z vyjádření
$$
\text{SST} = \text{SSR} + \text{SSE}
$$
je patrné, že změna v jednom součtů čtverců musí být doprovázena opačným vlivem (tedy jestli se [[Součet vysvětlených čtverců|SSE]] zvýší, [[Součet čtverců reziduí|SSR]] se musí snížit). V nejhorším (*teoretickém*) případě nově přidaná proměnná nevysvětlí vůbec nic nového, a součty čtverců zůstanou stejné. Pokud však vysvětli cokoliv dalšího, [[Součet vysvětlených čtverců|SSE]] se zvýší a tím pádem [[Součet čtverců reziduí|SSR]] se sníží.
## Intuice s optimalizací
Pokud si uvědomíme, že [[Regrese - Metoda nejmenších čtverců]] minimalizuje [[Součet čtverců reziduí|SSR]], po přidání další proměnné nemůže být hodnota vyšší - v tom případě by se $\beta$ spojená s novou proměnnou ,,nastavila" na 0 a [[Součet čtverců reziduí|SSR]] by bylo stejné.

> [!important] Důsledek
>  [[Součet čtverců reziduí|SSR]] tedy se tedy s novou vysvětlovanou proměnnou může pouze snížit. A jelikož [[Celkový součet čtverců|SST]] zůstává konstantní, znamená to, že [[Součet vysvětlených čtverců|SSE]] se může pouze zvýšit (nebo zůstat stejné).

- - -
# Literatura
