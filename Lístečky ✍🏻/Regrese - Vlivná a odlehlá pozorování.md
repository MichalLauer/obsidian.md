---
Datum: 2024-05-08
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Regrese
# Regrese - Vlivná a odlehlá pozorování
Vlivné a odlehlé pozorování není to samé a mělo by se mezi tím odlišovat.
**Vlivné pozorování**: zásadně mění tvar regresní přímky
**Odlehlé pozorování:** je odlehlé od dat, ale není vzdálené od regresní přímky
Můžeme měřit např. pomocí [[Regrese - Leverage]], [[Regrese - PRESS]], [[Regrese - Vnější studentizované residuum]], [[Regrese - Cookova vzdálenost]].
## Příklad
![[Pasted image 20240508150414.png]]

1) Odlehlé a nevlivné
2) Neodlehlé a nevlivné
3) Neodlehlé a vlivné
4) Odlehlé a vlivné

```r
library(ggplot2)
x <- rnorm(25, 5)
y <- 5 + 2 * x + rnorm(25)
l <- lm(y ~ x)
outliers <- data.frame(
  x = c(10, 5, 10, 5),
  y = c(27, 9, 10, 14.5),
  color = c("red", "green", "pink", "purple"),
  label = c(1, 3, 4, 2)
)
data.frame(x = x,
           y = y) |> 
  ggplot(aes(x = x, y = y)) +
  geom_point() +
  geom_abline(intercept = l$coefficients[1],
              slope = l$coefficients[2],
              linewidth = 1, col = "lightblue") +
  geom_smooth(se = F, method = "lm", formula = 'y ~ x',
              linewidth = 1) +
  geom_point(data = outliers, aes(color = color),
             show.legend = F) +
  geom_label(data = outliers, aes(label = label),
             nudge_x = .1, nudge_y = -.7) +
  theme_void()
```
- - -
# Literatura
