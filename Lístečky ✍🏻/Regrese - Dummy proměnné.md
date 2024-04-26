---
Datum: 2024-04-09
Typ:
  - Bibliografická
aliases:
 - Regrese - dummifikace
 - Regrese - indikátorové proměnné
---
*Klíčová slova:* #Regrese 
# Regrese - Dummy proměnné
V případě použití [[Regrese - Kategoriální proměnné|kategoriální proměnné]] je nutné kategorie rozdělit na $k - 1$ proměnných (indikátorů). Pokud je dané pozorování z $m$-té kategorie, $x_m = 1$, jinak se $x_m = 0$.
$$
y_i = \beta_0 + \sum_{m=1}^{k-1} x_{i, m}\delta_m + \epsilon_i
$$
 Referenční ($k-1$) kategorie je reprezentovaná $\beta_0$ a značí také **podmíněný** průměr. Koeficienty $\delta$ jsou pak **změnou vůči referenční kategorii**.
 
```r
data <- mtcars[,1:3]
data$cyl_4 <- as.integer(data$cyl == 4)
data$cyl_6 <- as.integer(data$cyl == 6)

mean(data$mpg[data$cyl == 4])
mean(data$mpg[data$cyl == 6])
mean(data$mpg[data$cyl == 8])
summary(lm(mpg ~ cyl_4 + cyl_6, data = data))
```

- - -
# Literatura
[[Malec2023_4ST426Regrese|MALEC, Lukáš, 2023. 4ST426 Regrese. In: . Prague University of Economics and Business.]]