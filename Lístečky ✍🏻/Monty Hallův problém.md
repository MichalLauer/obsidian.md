---
Datum: 2024-06-16
Typ:
  - Spojovací
aliases:
---
*Klíčová slova:* 
# Monty Hallův problém
Paradox z televizní show, kdy si účastník má za úkol vybrat jedny dveře, za kterými je auto - pokud si vybral správně, tak auto vyhraje. Host mu otevře jedny ze tří dvěří a ukáže, že za nimi auto není. Je pro účastníka lepší svoji volbu změnit a nebo zůstat na vybraných dveřích?
## Bayesovské řešení
Optimální řešení lze získat díky [[Bayes - Bayesův vzorec]] a rozhodovací tabulky. Hypotéza bude, že **Výhra je za dveřmi x**. Nasbíraná data jsou informace, které dveře si účastník vybral a za kterými dveřmi auto není.

|   Hypotéza<br>$H$    | Apriorní informace<br>$P(H)$ |
| :------------------: | :--------------------------: |
| Výhra je za dveřmi 1 |            $1/3$             |
| Výhra je za dveřmi 2 |            $1/3$             |
| Výhra je za dveřmi 3 |            $1/3$             |
Poté jsou nasbíraná data, např.:
- účastník si vybral první dveře, a
- moderátor otevřel druhé dveře, kde nic není.
Otázka, která je pro každé dveře položena je

> **Jaká je pravděpodobnost, po výběru prvních dveří moderátor otevře druhé dveře, za předpokladu, že výhra je za ... dveřmi?**

1) v tomto případě má na výběr druhé a třetí dveře, proto $P = 1/2$.
2) pokud je výhra za druhými dveřmi, pravděpodobnost, že je otevře, je nulová
3) v případě, že výhra je za třetími dveřmi a já si vybral první dveře, jediná možnost moderátora je otevřít dveře druhé, a tedy $P = 1$.

| Apriorní informace<br>$P(H)$ | Likelihood<br>$P(D\|H)$ | Posteriorní informace<br>$P(H)P(D\|H)$ | Posteriorní rozdělení<br>$P(H\|D)$ |
| :--------------------------: | :---------------------: | :------------------------------------: | :--------------------------------: |
|            $1/3$             |          $1/2$          |         $1/3 \times 1/2 = 1/6$         |       $1/6 \times 2/1 = 1/3$       |
|            $1/3$             |           $0$           |                  $0$                   |                $0$                 |
|            $1/3$             |            1            |          $1/3 \times 1 = 1/3$          |        $1/3 \times 2/1=2/3$        |

*pozn.: normalizační konstanta lze získat součtem posteriorní informace díky [[Pravděpodobnost - Celková pravděpodobnost|větě o celkové pravděpodobnosti]].*

Pro účastníka je tedy vždy vhodné svoji volbu změnit, jelikož pravděpodobnost, že auto je za druhými dveřmi, je $0,66$.