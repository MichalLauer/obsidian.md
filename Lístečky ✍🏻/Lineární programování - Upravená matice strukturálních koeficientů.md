---
Datum: 2024-02-28
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Optimalizace/LineárníProgramování 
# Lineární programování - Upravená matice strukturálních koeficientů

Občas se hodí převést si podmínky v rámci [[Lineární programování|lineárního programování]] na rovnost, tedy
 $$
\mathbb{A}x = b.
$$
Toho lze docílit přidáním jednotkové matice k naším datům, tedy
$$
\mathbb{A}'=(\mathbb{A} \space \mathbb{I}).
$$
Díky této transformaci se dostáváme z omezení
$$
a_1x_1 + a_2x_2 \geq b_1
$$
na omezení
$$
a_1x_1 + a_2x_2 + x_3 = b_2.
$$
$x_3$ zde značí jako přebytečná proměnná, která obsahuje záporný nadbytek v omezení.
- - -
# Literatura
[[Sokol2023_4EK632OptimalizacniModely|SOKOL, Ondřej, 2023. 4EK632 Optimalizační modely (v angličtině). In: . Prague University of Economics and Business.]]