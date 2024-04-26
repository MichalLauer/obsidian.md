---
Datum: 2024-04-20
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese 
# Regrese - Neklesající pokles indexu determinace
Pokud do [[Vícerozměrný regresní model]] přidáme *jakoukoliv* další vysvětlující proměnnou, [[Koeficient determinace]] nemůže nikdy klesnout. Je to z toho důvodu, že celá [[Regrese - Metoda nejmenších čtverců]] minimalizuje [[Součet čtverců reziduí|SSR]] a tedy vztah
$$
1 - \frac{\text{SSR}}{\text{SST}}
$$
nikdy neklesne, ale v nejhorším případě zůstane stejné (v tom případě bude koeficient asociovaný s novou proměnnou nulový).

> [!important] Důsledek
>  [[Součet čtverců reziduí|SSR]] tedy se tedy s novou vysvětlovanou proměnnou může pouze snížit. A jelikož [[Celkový součet čtverců|SST]] zůstává konstantní, znamená to, že [[Součet vysvětlených čtverců|SSE]] se může pouze zvýšit (nebo zůstat stejné).

- - -
# Literatura
