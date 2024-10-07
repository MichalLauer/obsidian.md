---
Datum: 2024-03-09
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese 
# Regrese - Metoda nejmenších čtverců
Odhady regresních koeficientů lze získat pomocí [[Optimalizace - Metoda nejmenších čtverců|metody nejmenších čtverců]], což je speciální tvar [[Regrese - Obecná metoda nejmenších čtverců|obecné metody nejmenších čtverců]]. Automaticky tedy předpokládáme [[Regrese - Předpoklad plné hodnosti]].
## Očekávaná hodnota koeficientů
Pro **nezkreslenost** je nutné dodržet předpoklady
- [[Regrese - Předpoklad linearity]]
- [[Regrese - Předpoklad náhodného výběru]]
- [[Regrese - Předpoklad exogenity chyb]]
Poté lze nezkreslenost dokázat jako
$$
E\left[\hat{\beta}\right] =
E\left[\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T\mathbb{y}\right] =
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^TE[\mathbb{X}\mathbb{\beta} + \mathbb{e}] =
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T\mathbb{X}\mathbb{\beta} =
\mathbb{\beta}.
$$
## Rozptyl koeficientů
Za platnosti [[Regrese - předpoklad homoskedasticity]] lze vyjádřit kovarianční matice odhadnutých koeficientů analyticky.
$$
\begin{align}
C(\hat{\beta}) &= C((\mathbb X^T \mathbb X)^{-1} \mathbb X y) \\
&= 
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T
\space C(y) \space
\left[\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T\right]^{T} = \\
&= \left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T
\space \sigma^2 \mathbb I \space
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
> Pokud předpoklad neplatí, odhady jsou stále nezkreslené, ale nemají nejmenší rozptyl.
# Residua
Residua jsou definována jako
$$
e = y - \hat y,
$$
nebo pomocí matice [[Regrese - Matice M|matice M]]
$$
\mathbb{e} = \mathbb{M}\mathbb{y} = \mathbb{M} \mathbb{\epsilon}.
$$
**Očekávaná hodnota** za platnosti [[Regrese - Předpoklad exogenity chyb]] je
$$
E(\mathbb{e}) = \mathbb{M} E(\mathbb{\epsilon}) = 0,
$$
a **nezkreslený odhad rozptylu** za předpokladu [[Regrese - Předpoklad homoskedasticity]] je
$$
\sigma^2 = \frac{Q(e)}{n - p}.
$$
**Kovarianční matice** pak za stejného předpokladu
$$
C(\mathbb{e}) = \mathbb{M} C(\mathbb{e}) \mathbb{M}^T = \sigma^2 \mathbb{M},
$$
což lze rozepsat dále 
$$
C(\mathbb{e}) = 
\begin{bmatrix} 
\sigma^2(1 - h_{11}) & -\sigma^2h_{12}      & \dots \\
-\sigma^2h_{21}      & \sigma^2(1 - h_{22})  & \dots \\
\vdots               & \vdots                & \ddots
\end{bmatrix}.
$$
Obecně lze tedy **rozptyl** $i$-tého residua zapsat jako $\sigma^2(1 - h_{ii})$ a **kovariance** jako $-\sigma^2h_{ij}$.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]
