**Designové váhy**
- každá jednotka má stejnou pravděpodobnost být ve výběru
- člověk má víc čísel - krát 1/počet telefony
**Populační váhy**
- podle počtu lidí v dané populaci
**Non-response váhy**
- pokud chybí "celý respondent", můžu na to hodit logistiku
**Kalibrační váhy / Post-stratifikační váhy**
- kalibrace vzhledem k známým proměnným
**Kombinace**
- nenásobit dohromady
- "nabalovat" - 
	- Váha na pohlaví, aplikuju
	- pak vážím na věk, aplikuju
	- pak vážím na kraj, aplikuju
	- pak aplikuju pohlaví.....
	- Aby to bylo stabilizované, dělám to pořád dokola
Vážením se zvětšuje rozptyl - Bias vs. variance
- Řezání vah, konzervativně $\langle 0.3; 3\rangle$
- Slučování kategorií - skupiny, které si budou podobné
Časté chyby
- průměr vah by měl být 1
- není přímočará aplikovatelnost