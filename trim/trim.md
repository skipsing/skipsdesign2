# Trim

## Innledning
Trim er en beskrivelse på et fartøys flytekondisjon. Ved null trim vil et fartøy ha samme dypgangsavlesning, $T$ både forut og akter.
Vi sier da at fartøyet flyter på *even keel*. 

I situasjoner der de hydrostatiske størrelsene $LCG$ og $LCB$ ikke er i samme punkt ved *even keel* vil fartøyet søke likevekt der disse er ovenfor hverandre. Tyngdepunktet er som regel *fast og stasjonært* så det vil være oppdriftsenteret som flytter på seg.

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/fartøy-søker-likevekt-ved-trim.PNG
---
align: center
--- 
Ved langskips ubalanse mellom $LCG$ og $LCB$ vil et fartøy trimme til $LCB$ er overrett med $LCG$
```

Fartøyet vil da rotere om en tverrskips akse, flotasjonsaksen. Vi sier fartøyet *trimmer* om flotasjonspunktet. Volumsenteret av det neddykkede volumet, $LCB$, vil da flytte seg mot den enden som får større dypgang.    


## Betegnelser for trim 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/betegnelser-trim.PNG
---
align: center
--- 
Dypgang akter $T_A$ og dypgang forut $T_F$
```

- Avlest dypgang akter: $T_A$ *(eng. draught aft)*
- Avlest dypgang forut: $T_F$ *(eng. draught forward)*
- Avlest dypgang midtskips: $T_M$ *(eng. draught midship)*


Avlesning av dypgang kan gjøres visuelt ved hjelp av påmalte/sveiste *fotmerker*. 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/fotmerker-trim.PNG
---
align: center
--- 
Her ser vi to eksempler midtskips til venstre og i baugen til høyre. 

```

```{admonition} Noen huskeregler 
:class: note

Fartøyets totale trim finner vi ved å ta differansen mellom trim akter og forut: 
- $ Trim = T_A-T_F $

Og er differanse null vil skipet ha null trim: 

- $ T_A = T_F  $ &rarr; Skipet har *null* trim. 

Er dypgangen større forut enn akter vil skipet ha en forlig trim: 

- $ T_A < T_F $ &rarr; Skipet har *forlig* trim. *(eng. forward trim)*

Motstatt er dypgangen større akter enn forut vil skipet ha en akterlig trim: 

- $ T_A > T_F $ &rarr; Skipet har *akterlig* trim. *(eng. aft trim)*

Dypgang midtskips finner en ved å ta gjennomsnitt av dypgang av forut og akter: 
- $ T_M = \frac{1}{2}(T_A + T_F) $

```

```{admonition} Fortegn 
:class: warning

Merk at fortegn på trim kan variere fra land til land og software til software. 
```

## Trim ved styrlast 

Definisjonen av trim måles fra *baseline*, (ikke fra kjølinjen). 
Fartøy med styrlast vil derfor *stikke dypere* akter enn forut ved null trim. 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/styrlast-trim.PNG
---
align: center
--- 
Måling av trim for fartøy med styrlast gjøres fra *baseline*
```

## Hydrostatiske størrelser for trim 
For å beregne et fartøys trim skal vi introdusere noen nye begreper og størrelser. Disse blir i all hovedsak generert av dataprogram (f.eks Maxsurf). 

(content:references:mct)=
### Enhetstrimmomentet

Enhetstrimmomentet, $MCT$, *(eng. Moment to Change Trim)* er momentet som skal til for at fartøyet skal trimme $1[cm]$. Ofte også benevnt $MCT_{1cm}$ eller $MT1cm$. 

$$ MCT_{1cm} = \frac{I_F \times \rho}{100 \times L_{pp}}[\frac{tm}{cm}] $$ 

der $ I_F  $ = Annet arealmoment av vannlinjen om tverrskipsnøytralakse, $LCF$. 

(content:references:tpc)=
### Tonn pr centimeter neddykking

Økt deplasement per cm neddykking, ofte referert til som *Tonnes per centimetre*, $TPC$ eller $TP_{1cm}$, og er definert som:  

$$ TP_{1cm} = \frac{A_{WL} \times \rho_{sea}}{1cm}[\frac{t}{cm}] $$

(content:references:lcf)=()
### Langskips flotasjonsenter 

Dette er ofte referert til som et punkt, men i teorien er det langskipsposisjon til en tverrskipsakse gjennom arealsenteret til vannlinjen, $A_{WL}$. 
Fartøyet vil trimme (rotere) om dette punktet. I figur under kan en se at for vanlige skrogformer vil LCF vanligvis ligge noe bak nullkryss, mens for en boksformet lekter vil det være i samme punkt. 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/lcf-lekter-skip.PNG
---
align: center
--- 
LCF's plassering i forhold til midtskip/nullkryss for ulike skrogformer
```

```{admonition} Regneeksempel $MCT_{1cm}$ for en boksformet lekter
:class: note

Vi har en boksformet lekter med følgende hoveddimensjoner: 
- $L_{pp} = 120[m]$, $B = 20[m]$ <br>

Siden lekteren har prismatiske sider trenger vi ingen ytterligere opplysninger for å beregne $MCT_{1cm}$ for alle mulig dypganger til lekteren. 

$$ MCT_{1cm} = \frac{I_F \times \rho}{100 \times L_{pp}}[\frac{tm}{cm}] $$

Beregner først annet arealmoment for en rektangulær vannlinje; $I_F = \frac{B \times L_{pp}^3}{12} $

$$ \downarrow $$

$$ MCT_{1cm} = \frac{\frac{B \times L_{pp}^3}{12} \times \rho}{100 \times L_{pp}}[\frac{tm}{cm}] $$

$$ \downarrow $$

$$ MCT_{1cm} = \frac{\frac{20[m] \times 120[m]^3}{12} \times 1.025[\frac{t}{m^3}]}{100[\frac{100[cm]}{m}] \times 120[m]} $$


$$ \downarrow $$

$$ MCT_{1cm} = 246\frac{[tm]}{[cm]} $$

Det vil si at vi må flytte $246[t]$ en avstand på $1[m]$ langskips for at den *totale* trimmen skal endre seg $1[cm]$. 
```


```{admonition} Regneeksempel $TP_{1cm}$ for en boksformet lekter
:class: note

Vi har den samme boksformet lekteren med følgende hoveddimensjoner: 
- $L_{pp} = 120[m]$, $B = 20[m]$ <br>

Siden lekteren har prismatiske sider trenger vi ingen ytterligere opplysninger for å beregne $TP_{1cm}$ for alle mulig dypganger til lekteren.  

$$ TP_{1cm} = \frac{A_{WL} \times \rho_{sea}}{1[cm]} $$

$$ \downarrow $$

$$ TP_{1cm} = \frac{L_{pp} \times B \times \rho_{sea}}{1[cm]} $$

$$ \downarrow $$

$$ TP_{1cm} = \frac{120[m] \times 20[m] \times 1.025\frac{[t]}{m^3}}{100\frac{[cm]}{[m]}} $$

$$ \downarrow $$

$$ TP_{1cm} = 24.6\frac{[t]}{[cm]} $$

Det vil si at vi må laste på lekteren $24.6[t]$ for å få en dypgangsendring på $1[cm]$

```

## Hydrostatiske tabeller 

Å beregne de hydrostatiske strørrelsene for trim manuelt vil være tungvindt og kreve endel tid. Stabilitetsprogrammene gjør dette mer eller mindre automatisk, og presenterer størrelsene i tabellform på en oversiktlig måte. 

Under er det vist et eksempel på en hydrostatisk tabell for tråleren M/S Havbryn. 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/hydrostatisk-tabell-havbryn.PNG
---
align: center
--- 
Hydrostatikktabell M/S Havbryn 
```

## Beregning av trim

Som vi husker fra tverrskipstabilitet der krenging ved store vinkler føre til at de hydrostatiske verdiene endrer seg pga skrogformen. Det samme gjelder for trim. Her skiller vi mellom trim forårsaket av *små vekter* og *store vekter* 

## Beregning av trim ved små vekter 
Små vekter er vekter som er så små at de ikke endrer de hydrostatiske verdiene signifikant ved lasting/lossing av vekten. (Tommelfingerregel er maks 10 % av deplasementet, men det kommer også an lengden på armen)

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/trim-små-vekter.PNG
---
align: center
--- 
Trimmomentet blir beregnet ut fra vektens posisjon fra LCF 
```


__Prosedyre__

1. Legg vekten i *LCF*.
2. Beregn parallel neddykking $\delta T=\frac{W}{TP_{1cm}} $ (eller les ut av hydrostatikktabell).
3. Flytt vekten til endelig posisjon og beregn trimmende moment $ M_T = W \times h $.
4. Bestem enhetstrimmomentet $ MCT_{1cm} = \frac{I_F \times \rho}{100 \times L_{pp}}[\frac{tm}{cm}] $. (eller les ut av hydrostatikktabell).
5. Beregn total trim $ t = \frac{M_T}{MCT_{1cm}}$. 
6. Fordel trim forut og akter:
 - $ t_a = LCF \times \frac{t}{L_{pp}} $
 - $ t_f = (L_{pp} - LCF ) \times \frac{t}{L_{pp}} $
7. Beregn nye dypganger forut og akter:
 - $ T_A = T_0 + \delta T \pm t_a $
 - $ T_F = T_0 + \delta T \pm t_f $


## Beregning av trim ved store vekter 
Store vekter er vekter som er så store at vil endre de hydrostatiske verdiene i vesentlig grad. (Tommelfingerregel her er fra 10 % av deplasementet og utover, men det kommer også an lengden på armen)

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/trim-store-vekter.PNG
---
align: center
--- 
Trimmomentet blir beregnet ut fra avstanden mellom *LCB* og *LCG* for fartøyet etter lasting. 

```


__Prosedyre__

1. Legg den store vekten til utgangsdeplasementet og etabler nytt deplasement $ \Delta_1 $.  
2. Beregn nytt felles langskips vektstyngdepunkt $ LCG_1 $.
3. Etabler dypgang $ T_1 $ for nytt deplasement ved *even-keel* tilstanden. 
4. Bestem følgende hydrostatiske verdier ved den nye dypgangen (fra hydrostatiske tabeller, kurvebladet eller direkte opplysninger):
 - Langskips oppdriftsenter *LCB*
 - Langskips flotasjonssenter *LCF*
 - Enhetstrimmomentet $ MCT_{1cm} $
5. Beregn trimmende moment som er vektdeplasementet multiplisert med trimarm $ \overline{BG} $, altså avstanden mellom $ LCG_1 $ og $ LCB $. $$ M_T = \Delta_1 \times \overline{BG_1} $$ 
6. Beregn total trim $ t = \frac{M_T}{MCT_{1cm}}$.
7. Fordel trim forut og akter:
 - $ t_a = LCF \times \frac{t}{L_{pp}} $
 - $ t_f = (L_{pp} - LCF ) \times \frac{t}{L_{pp}} $
8. Beregn nye dypganger forut og akter:
 - $ T_A = T_1 \pm t_a $
 - $ T_F = T_1 \pm t_f $


## Eksempel trim ved store vekter 

Tråleren M/Tr Havstrand flyter på $T_M = 5.0[m]$ og på *even-keel*. Regellengden $L_{pp}=61.2[m]$
Det fylles 400[t] frossen fisk i lasterommet med $LCG_{last} = 35[m]$ forenfor A.P.     

Basert på hydrostatikktabellen under skal nye dypganger forut og akter beregnes. 

 ## Øvinger 

 <a href="https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/trim-north-pomor.ipynb" download>Øving trim North Pomor</a>
