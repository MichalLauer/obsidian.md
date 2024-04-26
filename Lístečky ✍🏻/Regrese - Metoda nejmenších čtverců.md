---
Datum: 2024-03-09
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese 
# Regrese - Metoda nejmenších čtverců
Odhady regresních koeficientů lze získat pomocí [[Optimalizace - Metoda nejmenších čtverců|metody nejmenších čtverců]]. Automaticky tedy předpokládáme [[Regrese - Předpoklad plné hodnosti]].
## Nezkreslenost koeficientů
Pro **nezkreslenost** je nutné navíc dodržet předpoklady
- [[Regrese - Předpoklad linearity]]
- [[Regrese - Předpoklad náhodného výběru]]
- [[Regrese - Předpoklad exogenity chyb]]
Poté lze nezkreslenost odvodit jako
$$
E\left[\hat{\beta}\right] =

E\left[\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T\mathbb{y}\right] =
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^TE[\mathbb{X}\mathbb{\beta} + \mathbb{e}] =
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T\mathbb{X}\mathbb{\beta} =
\mathbb{\beta}
$$
## Rozptyl koeficientů
Za platnosti [[Regrese - předpoklad homoskedasticity]] lze vyjádřit kovarianční matice odhadnutých koeficientů vyjádřit analyticky.
$$
\begin{align}
C(\hat{\beta}) &= C((\mathbb X^T \mathbb X)^{-1} \mathbb X y) \\
&= 
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T
\space C(y) \space
\left[\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T\right]^{T} = \\
&= \left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T
\space \sigma^2 \space
\mathbb{X}\left(\mathbb{X}^T\mathbb{X}\right)^{-1} = \\
&= \sigma^2 \space
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T
\mathbb{X}\left(\mathbb{X}^T\mathbb{X}\right)^{-1} = \\
&= \sigma^2 \space
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}
\end{align}
$$
$\sigma^2$ je vyjádřena díky [[Regrese - rozptyl závislé proměnné]]. Individuální rozptyl lze označit jako 
$$
D(\beta_j) = \sigma^2 a_{jj},
$$
kde $a_{jj}$ značí hodnotu na diagonále matice $(\mathbb X^T \mathbb X)^{-1}$.

> [!warning] Nezkreslenost
> Pokud předpoklad neplatí, odhady jsou stále nezkreslené, ale nemají nejmenší rozptyl
## Rozptyl residuí
Rozptyl lze odhadnout jako
$$
\hat\sigma^2 = \frac{Q(e)}{n - p}.
$$
Pokud platí [[Regrese - předpoklad homoskedasticity]], odhad je **nezkreslený**. Kvadratická forma residuí lze také vyjádřit pomocí [[MLR - Matice M|matice M]]
$$
Q(e) = e^Te = (\mathbb{M}\mathbb{y})^T\mathbb{M}\mathbb{y} =
\mathbb{y}^T\mathbb{M}^T\mathbb{M}\mathbb{y} = \mathbb{y}^T\mathbb{M}\mathbb{y}.
$$
Rozptyl jednotlivých residuí je pak $D(e_i) = \sigma^2(1 - h_{ii})$.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
