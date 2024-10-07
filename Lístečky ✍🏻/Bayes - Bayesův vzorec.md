---
Datum: 2024-06-16
Typ:
  - Bibliografická
aliases:
---
*Klíčová slova:* #Bayes
# Bayes - Bayesův vzorec
Identický vzorec jako [[Pravděpodobnost - Bayesův vzorec]], akorát bere v potaz data $D$ a hypotézu $H$.
$$
P(H|D)=\frac{P(H)P(D|H)}{P(D)}=\frac{P(D|H)P(H)}{\int P(D|H)P(D)}
$$
Bavíme se tedy o **pravděpodobnosti nějaké hypotézy po nasbírání dat**.
- $P(H)$ - pravděpodobnost samotné hypotézy, **apriorní rozdělení**
- $P(D|H)$ - pravděpodobnost nasbíraných dat za předpokladu, že hypotéza platí - **věrohodnost (likelihood)**
- $P(D)$ - pravděpodobnost nasbíraných dat, **normalizační konstanta**