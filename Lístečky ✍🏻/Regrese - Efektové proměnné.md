---
Datum: 2024-04-09
Typ:
  - Bibliografická
aliases:
 - Regrese - contrast effects
 - Regrese - kontrastní proměnné
---
*Klíčová slova:* #Regrese 
# Regrese - Efektové proměnné
Pokud se v regresi používá [[Regrese - Kategoriální proměnné|kategoriální proměnná]], je třeba ji pro účely regrese transformovat. V případě efektového kódování se $k$ kategorií promění na $k - 1$ proměnných. Pokud dané pozorování patří do kategorie, $x_m = 1$, jinak $x_m = 0$. **Narozdíl od [[Regrese - Dummy proměnné|dumifikace]] se referenční kategorie řeší jinak**. Pokud pozorování patří do referenční kategorie, $x_m = -1; m = 1, 2, \dots, k - 1$.
$$
y_i = \beta_0 + \sum_{m=1}^{k-1} x_{i, m}\delta_m + \epsilon_i
$$

$\beta_0$ značí **průměr z podmíněných středních hodnot** vysvětlované proměnné. Střední hodnota nereferenčních kategorií je vyjádřena jako $\beta_0 + \delta_m$. Střední hodnota referenční kategorie je pak $\beta_0 - \sum_{m=1}^{k - 1} \delta_m$.

```r
data <- mtcars[,1:3]
data$cyl_4 <- as.integer(data$cyl == 4)
data$cyl_6 <- as.integer(data$cyl == 6)
data$cyl_4 <- ifelse(data$cyl == 8, -1, data$cyl_4)
data$cyl_6 <- ifelse(data$cyl == 8, -1, data$cyl_6)

mean(c(
  mean(data$mpg[data$cyl == 4]),
  mean(data$mpg[data$cyl == 6]),
  mean(data$mpg[data$cyl == 8])))
mean(data$mpg[data$cyl == 4])
mean(data$mpg[data$cyl == 6])
mean(data$mpg[data$cyl == 8])
summary(lm(mpg ~ cyl_4 + cyl_6, data = data))

```

- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]