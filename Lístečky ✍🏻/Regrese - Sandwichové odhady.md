---
Datum: 2024-06-01
Typ:
  - Bibliografické
aliases: 
---
*Klíčová slova:* #Regrese 
# Regrese - Sandwichové odhady
V případě, nejsou splněny [[Regrese - Gauss-Markův teorém|předpoklady]] o chybové složce regresního modelu lze odhady upravit tak, aby byli konzistentní a nabízeli spolehlivější inferenci. Kovarianční matici odhadnutých koeficientů lze obecně zapsat jako
$$
c(\epsilon) = \Omega = \sigma^2 \mathbb W.
$$
V případě, kdy jsou splněné předpoklady, se $\mathbb W = \mathbb I$. V opačném případě nelze rozptyl odhadnutých koeficientů zjednodušit a dostáváme
$$
C(b) = \sigma^2 \space
\left(\mathbb{X}^T\mathbb{X}\right)^{-1}\mathbb{X}^T W
\mathbb{X}\left(\mathbb{X}^T\mathbb{X}\right)^{-1}.
$$
V takovém případě lze odhadnout kovarianční matici $\Omega$ pomocí speciálních sandwichových odhadů.
## Vlastnosti
Použití metody nemění nic na zkreslenosti (resp. nezkreslenosti) odhadů a opravuje pouze kovarianční matici odhadů. Díky tomu je inference robustnější., obecně jsou však chyby větší.
- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]