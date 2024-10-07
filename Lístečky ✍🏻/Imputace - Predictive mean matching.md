---
Datum: 2024-09-29
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Imputace
# Predictive mean matching
Metoda, díky které lze imputovat chybějící hodnoty a zároveň je zachováno rozdělení a specifika *(horní/spodní hranice, diskrétnost...)* dané proměnné.
## Postup
Nechť je proměnná $x$ která obsahuje chybějící proměnné a proměnné $z_1, \dots, z_p$, které jsou kompletní. Prvním krokem je vytvoření pomocné regrese
$$
x = \hat\beta_1 z_1 + \dots + \hat\beta_p z_p.
$$
Odhadnuté koeficient $\hat\beta$ a jejich kovarianční matice $\text{var}(\hat\beta)$  jsou použité ve vícerozměrném normálním rozdělení, ze kterého jsou generované nové odhady.
$$
\beta^*\sim N_p(\hat\beta, \text{var}(\hat\beta))
$$
Pomocí nových odhadnutých koeficientů jsou vytvořené nové predikce pro $x$.
$$
x^* = z * \beta^*
$$
V této situaci jsou některá $x_n$ chybějící, ale $x^*_n$ predikovaní. Nyní se určí libovolná hranice $\ell$, podle které se najdou nejbližší pozorování k $x^*_n$. Z vybraných nejbližších pozorování k $x^*_n$ je náhodně vybráno jedno pozorování, kterého $x_i$ hodnota nahradí chybějící hodnotu. **Imputovaná hodnota je tedy z původního sloupečku $x$ a ne z predikcí $x^*$.**
- - -
# Literatura
[[Formanek2024_4EK417PraktikumEkonometrie|FORMÁNEK, Tomáš, 2024. 4EK417 Praktikum z ekonometrie. In: . Prague University of Economics and Business.]]