

# Stabilitet ved skade 
## Prosedyre for å beregne stabilitet etter skade 

- 



Stabilitet ved skade og overfylling

Vi har i de foregående kapitelene diskutert oppdrift og stabilitet for skip som er _intakt_. 

Ulykkesscenarioer som et skip kan komme ut for

- grunnstøting
- kollisjon 
- utilsiktet fylling 

Ved grunnstøting eller kollisjon kan et eller flere områder av skipet punkteres fra utsiden og fylles da med (sjø)vann fra omgivelsene. Trykket på innsiden blir da utlignet med det eksterne (hydrostatiske)trykket og volumet vil ikke bidra som oppdriftsgivende.  

Ved en reduksjon av fartøyets oppdriftsgivende volum vil det være en ubalanse mellom vekt og oppdrift. Fartøyet vil da søke en ny likevektsposisjon, der en eller flere av følgende verdier må ha endret seg: 

- Dypgang
- Trim 
- krenging (slagside)

```{note}
I sære tilfeller overfyller man et eller flere av fartøyets oppdriftsgivende volumer i den hensikt å senke skipet. Det kalles også å *[bore i senk](https://no.wikipedia.org/wiki/Bore_i_senk)* eller *scuttling* på engelsk. 
```


** Myndighetenes krav til stabiliet ved skade **

I dette emnet setter vi følgende kriterier for skadet tilstand

- $GM_{T_{skade}} > 0m $ 
- Dekkshjørnet skal ikke være neddykket i skadet likevektstilstand 

## Tapt oppdrifts metoden 

Ved tapt oppdriftsmetode er $\delta$ uendret. Fartøyet får dermed en ny dypgang $T_s$ etter skade.

__Prosedyre__

1. Beregn ny dypgang i skadet tilstand $T_s$ ved å sette $\delta_{intakt} = \delta_{skadet}$ 
2. Beregn fartøyets trim som følge av skade. parallel neddykking $\delta T=\frac{W}{TP_{1cm}} $ (eller les ut av hydrostatikktabell).
3. Flytt vekten til endelig posisjon og beregn trimmende moment $ M_T = W \times h $.
4. Bestem enhetstrimmomentet $ MCT_{1cm} = \frac{I_F \times \rho}{100 \times L_{pp}}[\frac{tm}{cm}] $. (eller les ut av hydrostatikktabell).
5. Beregn total trim $ t = \frac{M_T}{MCT_{1cm}}$. 
6. Fordel trim forut og akter:
 - $ t_a = LCF \times \frac{t}{L_{pp}} $
 - $ t_f = (L_{pp} - LCF ) \times \frac{t}{L_{pp}} $
7. Beregn nye dypganger forut og akter:
 - $ T_A = T_0 + \delta T \pm t_a $
 - $ T_F = T_0 + \delta T \pm t_f $


