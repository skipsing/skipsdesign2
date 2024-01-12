


# Lastkondisjoner

En lastekondisjon for et skip er en sammenstilling av alle vektene med tilhørende tyngdepunktsplasseringer som i et gitt tidspunkt utgjør skipets *vektsdeplasement*

Vi repeterer her *lettskip* og *dødvekt* (linke) 

$$ \Delta = W_{lettskip} + W_{dødvekt}  $$

## Lettskipet

Lettskipsvekten $ W_{lettskip} $ består av vekten til *tomt* skip; på komponentform vekten av skrog, utrustning og maskineri. 

## Dødvekten

Dødvekten består av to bidrag; vekt av forbruksvarer (*eng:consumables*) og vekt av personer og last (*eng:[Payload](#payload)*)  


### Variable vekter (ikke inntektsgivende) ####
Dette er forbruksvarer som er ment for fartøyets eget forbruk og som vil variere etter blant annet seilingsdistanse. 

Eksempler på forbruksvarer:
- proviant
- vann
- drivstoff 
- smørolje
- forbruksmateriell 
- reservedeler

### Inntektsgivende vekter ####

For et handelsfartøy er vekten av lasten det største bidraget av dødvekten. Eksempler på last: 
- Olje for et tankskip
- Jernmalm for et bulkskip
- Containere for et containerskip 
- Biler for en bilferge


```{tip} Payload
:name: payload

Det engelske ordet payload referer til den inntektsgivende lasten som transporteres og/eller de betalende passasjerene.

```

```{note} Inngangsverdier ved design av et nytt skip
:name: hva-bestemmer-rederiet

Når et rederi skal *kontrahere* et nytt skip vil fart, lastekapasitet og seilingsdistanse (uten etterfylling) være sentrale inngangsverdier som de krever at fartøyet skal kunne oppfylle.

- seilingsdistanse og fart vil her gi minimumsverdier på drivstoffkapasitet, ferskvannskapasitet og proviant. Her brukes ofte enhetene *nautisk mil* på distanse og *knop* i.e *nautisk mil per time* på fart. Antall timer i seilas får en da ved;   

$$\delta_{seilas} = \frac{distanse[nm]}{ fart[\frac{nm}{h}]}$$

- lastkapasitet vil gi minimumsverdi for størrelse på lasterommet, og som igjen vil sterkt påvirke valg av *hoveddimensjoner*. 
```

```{tip} Lastekapasitet
:name: lastekapasitet-betydning

Definisjon på lastekapasitet skiller mellom: 
- Vektkapasitet
- Volumkapasitet. Varer eller gods med lav egenvekt vil 

```
#### Tyngdepunkt

Alle vektene som utgjør lettskipet og dødvekten har sine spesifikke tyngdepunkter i skipets referansesystem. 

```{admonition} Eksempel tyngdepunktsberegning lettskip
:class: tip 
:class: dropdown
:name: lettskipstyngdepunkt

Lasteskipet har under bygging fått veid forskip, midtskip, akterskip og overbygg ved hjelp av kranløft. I tillegg er vekta av kran og hovedmotor kjent.  

| Lengde      | Lpp  | 125      | m    |
| ----------- | ---- | -------- | ---- |
| Bredde      | B    | 18       | m    |
| Dypgang     | Tdwl | 7.5      | m    |
| Blokk       | CB   | 0.75     | \-   |
| Dybde       | D    | 11       | m    |
| Deplasement |      | 12972.66 | tonn |
| Fart        | V    | 14       | kn   |
|             |      | 7.202222 |      |
| Froudetall  |      | 0.205673 | \-   |
| L/B forhold |      | 6.944444 |      |
|             |      |          |      |
| Payload     |      | 8000     | tonn |
| Forbruk     |      | 1000     | tonn |
| Lettskip    |      | 4000     | tonn |
| Antatt depl |      | 13000    |      |

Dette kan løses manuelt i regnearket ved hjelp av tyngdepunktssatsen

$$ X_{G_{tot}} = \frac{\sum \limits}{3} $$


```

$$ 3 \times 3 $$

Når vekt og tyngdepunkt er kjent kan en regne skipets dypgang og tilhørende stabilitetsegenskaper. 

:::{tip}
:class: myclass1,myclass2
:name: a-tip-reference
Let's give readers a helpful hint!
:::


Et skip vil i de fleste sammenhenger kunne ha mange ulike *lastkondisjoner*. En lastkondisjon er en sammensatt 