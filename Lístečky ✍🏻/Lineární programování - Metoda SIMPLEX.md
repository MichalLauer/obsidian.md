---
Datum: 2024-02-28
Typ:
  - Bibliografická
  - Permanentní
  - Spojovací
aliases:
---
*Klíčová slova:* #Optimalizace/LineárníProgramování  
# Lineární programování - Metoda SIMPLEX
Metoda slouží k optimalizaci řešení problému z [[Lineární programování|lineárního programování]]. V rámci metody se používá maticová algebra k úpravě matice obsahující [[Lineární programování - Upravená matice strukturálních koeficientů|upravenou matici strukturálních koeficientů]] a cílovou funkci.
$$
\begin{bmatrix}
\mathbb{A} & \mathbb{I} & b \\
-c         & 0          & 0
\end{bmatrix}
$$
Před zahájením je nutné najít základní přípustné řešení. Většinou předpokládáme, že se jedná o střed souřadnic, tedy $(0, 0, \dots, 0)$.
Postup je následující:
1) Podle posledního řádku se vybere sloupeček $x$, který obsahuje nejmenší hodnotu
2) Pro každý řádek (kromě posledního) se vypočítá proměnná $b/a$, kde $a$ je omezení z vybraného sloupce
3) Řádek, který obsahuje nejmenší hodnotu $t$ se použije k vynulování posledního řádku
	1) vynásobení a přičtení řádků
4) Proces se opakuje do té doby, než jsou v posledním řádku u proměnných $x$ samé nuly
5) V tomto případě je hodnota $b$ optimální hodnotou cílové funkce
6) Hodnoty u přebytečných proměnných obsahují [[Lineární programování - Stínové ceny]]

- - -
# Literatura
[[Sokol2023_4EK632OptimalizacniModely|SOKOL, Ondřej, 2023. 4EK632 Optimalizační modely (v angličtině). In: . Prague University of Economics and Business.]]
