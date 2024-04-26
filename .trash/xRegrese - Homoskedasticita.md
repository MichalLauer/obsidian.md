---
Datum: 2023-12-28
Typ:
  - Permanentní
aliases:
---
*Klíčová slova:* #Regrese #Rozptyl
# Homoskedasticita
Obecně značí konstantní rozptyl reziduí v regresi (Wooldridge 2020, s. 45).
$$
Var(\textbf{u} | \mathbb{X}) = \sigma^2 
$$
Z [[Rozptyl - Pomocí očekávaných hodnot]] lze rozepsat jako
$$
Var(\textbf{u} | \mathbb{X}) = E(\textbf{u}^2) - E(\textbf{u})^2,
$$
jelikož jsou [[Regrese - Nezávislost residuí|residua nezávislá]], pak
$$
Var(\textbf{u} | \mathbb{X}) = E(\textbf{u}^2) = \sigma^2.
$$
- - -
# Literatura
[[Wooldridge2020_IntroductoryEconometricsModern|WOOLDRIDGE, Jeffrey M., 2020. Introductory econometrics: a modern approach. Seventh edition. Boston, MA: Cengage. ISBN 978-1-337-55886-0.]]
