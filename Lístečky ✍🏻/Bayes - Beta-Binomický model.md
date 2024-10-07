---
Datum: 2024-06-17
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Bayes
# Bayes - Beta-Binomický model
Rozdělení [[Rozdělení - Beta|beta]] a [[Rozdělení - Binomické|binomické]] jsou [[Bayes - konjugované rozdělení|konjugované]] a díky tomu lze vytvořit jednoduchý model. Nejčastěji se používá v případě, kdy **chceme odhadnout poměr (pravděpodobnost) události.**
## Věrohodnost
Za předpokladu nějaké pravděpodobnosti lze vyjádřit pravděpodobnost dat pomocí binomického rozdělení.
$$
P(D|H)=P(N, k|\pi)={N \choose k} \pi^k (1 - \pi)^{N - k}
$$
$k$ zde značí počet **úspěšených** pokusů a $N - k$ počet **neúspěšných** pokusů.
## Apriorní rozdělení
Pro apriorní rozdělení lze použít rozdělení beta, které je definované na intervalu $\langle 0, 1\rangle$.
$$
P(H) = p(\pi | \alpha, \beta)=\frac{\pi^{\alpha - 1}(1-\pi)^{\beta-1}}{B(\alpha, \beta)}
$$
## Sdružená pravděpodobnost
Po vynásobení $P(H)P(D|H)$ dostáváme
$$
\begin{align}
\frac{\pi^{\alpha - 1}(1-\pi)^{\beta-1}}{B(\alpha, \beta)}
\times
{N \choose k} \pi^k (1 - \pi)^{N - k} &= \\
\frac{{N \choose k}}{B(\alpha, \beta)} \pi^{(k + \alpha) - 1} (1 - \pi)^{(N - k + \beta) - 1}.
\end{align}
$$
## Posteriorní rozdělení
Nejprve je nutné získat $P(D)$
$$
\begin{align}
P(D) &= \int_0^1 P(D|H)P(H) \tag{1}\\
&= \int_0^1
{N \choose k} \pi^k (1 - \pi)^{N - k} 
\frac{\pi^{\alpha - 1}(1-\pi)^{\beta-1}}{B(\alpha, \beta)} \\
&= \frac{{N \choose k}}{B(\alpha, \beta)}
\int_0^1 \pi^k (1 - \pi)^{N - k}  \pi^{\alpha - 1}(1-\pi)^{\beta-1} \\
&= \frac{{N \choose k}}{B(\alpha, \beta)}
\int_0^1 \pi^{(k + \alpha)-1} (1 - \pi)^{(N - k + \beta) - 1}  \tag{2}\\
&= \frac{{N \choose k}}{B(\alpha, \beta)} B(k + \alpha, N - k + \beta)
\end{align}
$$
Krok (1) lze provést díky [[Pravděpodobnost - Celková pravděpodobnost|celkové pravděpodobnosti]] a krok (2) díky definici [[Beta funkce]]. Po dosazení do [[Bayes - Bayesův vzorec|bayesova vzorce]] dostáváme
$$
\frac
{
\frac{{N \choose k}}{B(\alpha, \beta)} \pi^{(k + \alpha) - 1} (1 - \pi)^{(N - k + \beta) - 1}
}
{
\frac{{N \choose k}}{B(\alpha, \beta)} B(k + \alpha, N - k + \beta)
} =
\frac
{
\pi^{(k + \alpha) - 1} (1 - \pi)^{(N - k + \beta) - 1}
}
{
B(k + \alpha, N - k + \beta)
} =
Beta(k + \alpha, N - k + \beta).
$$

> [!NOTE] Závěr
> Pokud budeme mít apriorní rozdělení $Beta(\alpha, \beta)$ a k popisu dat použijeme $Bin(k, N)$, posteriorní rozdělení bude $Beta(\alpha + k, \beta + N - k)$.

- - -
# Literatura
https://stats.stackexchange.com/questions/475959/beta-binomial-conjugate-proof