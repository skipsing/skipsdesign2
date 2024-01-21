# Trim

## Innledning
Trim er en beskrivelse på et fartøys flytekondisjon. Ved null trim vil et fartøy ha samme dypgangsavlesning, $T$ både forut og akter.
Vi sier da at fartøyet flyter på *even keel*. 

I situasjoner der de hydrostatiske størrelsene $LCG$ og $LCB$ ikke er i samme punkt ved *even keel* vil fartøyet søke likevekt der disse

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/fartøy-søker-likevekt-ved-trim.PNG
:scale: 50 %

Ved langskips ubalanse mellom $LCG$ og $LCB$ vil et fartøy trimme til $LCB$ er overrett med $LCG$
```

Fartøyet vil da rotere om en tverrskips akse, flotasjonsaksen. Vi sier fartøyet *trimmer* om flotasjonspunktet. Volumsenteret av det neddykkede volumet, $LCB$ vil da flytte seg mot den enden som får større dypgang.    


## Betegnelser for trim 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/betegnelser-trim.PNG
:scale: 50 %

Dypgang akter $T_A$ og dypgang forut $T_F$
```

- Avlest dypgang akter: $T_A$ *(eng. draught aft)*
- Avlest dypgang forut: $T_F$ *(eng. draught forward)*
- Avlest dypgang midtskips: $T_M$ *(eng. draught midship)*



Avlesning av dypgang kan gjøres visuelt ved hjelp av påmalte/sveiste *fotmerker*. 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/fotmerker-trim.PNG
:scale: 50 %
 
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
:scale: 50 %
 
Måling av trim for fartøy med styrlast gjøres fra *baseline*
```

## Hydrostatiske størrelser for trim 
For å beregne et fartøys trim skal vi introdusere noen nye begreper og størrelser. Disse blir i all hovedsak generert av dataprogram (f.eks Maxsurf). 

### Enhetstrimmomentet

Enhetstrimmomentet, $MCT$, *(eng. Moment to Change Trim)* er momentet som skal til for at fartøyet skal trimme $1[cm]$. Ofte også benevnt $MCT_{1cm}$ eller $MT1cm$. 

$$ MCT_{1cm} = \frac{I_F \times \rho}{100 \times L_{pp}}[\frac{tm}{cm}] $$ 

der $ I_F  $ = Annet arealmoment av vannlinjen om tverrskipsnøytralakse, $LCF$


### Tonn pr centimeter neddykking

Økt deplasement per cm neddykking, ofte referert til som *Tonnes per centimetre*, $TPC$ eller $TP_{1cm}$, og er definert som:  

$$ TP_{1cm} = \frac{A_{WL} \times \rho_{sea}}{1cm}[\frac{t}{cm}] $$

- Langskips flotasjonsenter 

Dette er ofte referert til som et punkt, men i teorien er det langskipsposisjon til en tverrskipsakse gjennom arealsenteret til vannlinjen, $A_{WL}$. 
Fartøyet vil trimme (rotere) om dette punktet. I figur under kan en se at for vanlige skrogformer vil LCF vanligvis ligge noe bak nullkryss, mens for en boksformet lekter vil det være i samme punkt som nullkryss.  

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/trim/images/lcf-lekter-skip.PNG
:scale: 50 %
 
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

$$ MCT_{1cm} = 246\frac{[tm]}{[m]} $$

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
:scale: 50 %
 
Hydrostatikktabell M/S Havbryn 
```