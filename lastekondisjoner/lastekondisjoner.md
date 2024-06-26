---
title: Lastekondisjoner
license: CC-BY-4.0
github: https://github.com/skipsing/skipsdesign2.git
authors:
  - name: Lars Erik Nygård 
    email: lars.e.nygard@ntnu.no
    affiliations:
      - NTNU i Ålesund
  - name: Håvard Vollset Lien (basert på og videreutviklede forelesningsnotater)
date: 2024/01/12
---

(section-label)=
# Lastekondisjoner

## Introduksjon
En lastekondisjon for et skip er en sammenstilling av alle vektene med tilhørende tyngdepunktsplasseringer som i et gitt tidspunkt utgjør skipets *vektsdeplasement*. 
 
Vi repeterer her *lettskip* og *dødvekt*:

$$ 
\Delta = W_{lettskip} + W_{dødvekt}  
$$

## Lettskipet
Lettskipsvekten $ W_{lettskip} $ består av vekten til *tomt* skip; på komponentform vekten av skrog, utrustning og maskineri. 

## Dødvekten
Dødvekten består av to bidrag; vekt av skipets egne forbruksvarer (*eng:consumables*) og vekt av personer og last (*eng:Payload*)  

For et handelsfartøy vil vekten av lasten være det største bidraget av dødvekten. Eksempler på last kan være: 
- Olje for et tankskip
- Jernmalm for et bulkskip
- Containere for et containerskip 
- Biler for en bilferge

```{admonition} Payload
:class: tip
Det engelske ordet payload referer til den inntektsgivende lasten som transporteres
```

Eksempler på fartøyets egne forbruksvarer:
- proviant
- vann
- drivstoff 
- smørolje
- forbruksmateriell 
- reservedeler

Disse vil variere iløpet av en seilas, og kapasiteten er blant annet avhengig av ønsket seilingsdistanse. 

```{admonition} Eksempelberegning vektdeplasement 
:class: note 
:name: eksempelberegning-vektdeplasement

Tørrlastskipet *M/S Freighter* ligger til kai og laster ombord $500[t]$ med last. Samtidig blir det bunkret $150[t]$ ferskvann. Lettskipvekten er oppgitt til å være $1250[t]$. Beregn skipets vektdeplasement når den er ferdig lastet. 

Vi har at $ \Delta = W_{lettskip} + W_{dødvekt}  $, og innsatt får vi:

$$ 
\Delta = W_{lettskip} + W_{ferskvann} + W_{payload} 
$$

$$ 
\Delta = 1250[t] \times 150[t] \times  500[t] 
$$

$$ 
\Delta = 1900[t] 
$$
 
```

## Tyngdepunkt
Alle vekter som tilsammen utgjør *lettskipet* og *dødvekten* har sine spesifikke tyngdepunkter utrykt i skipets eget referansesystem: 

- Vertikalt, $VCG$ -*Vertical Centre of Gravity*
- Langskips, $LCG$ -*Longitudinal Centre of Gravity*
- Tverrskips, $TCG$ -*Transverse Centre of Gravity*

```{admonition} Eksempelberegning samlet tyngdepunkt 
:class: note 
:name: eksempelberegning-tyngdepunkt

Vi bruker tyngdepunktssatsen for å finne samlet langskips tyngdepunkt for den oppgitte lastekondisjonen:

$$ 
LCG_{lastekondisjon} = \frac{\sum \limits_i^n(m_i\times x_i)}{\sum \limits_i^n( m_i)} 
$$

og der $x_i$ er avstand fra vekten $m_i$'s tyngdepunkt til skipets felles referansepunkt spant 0 i langskipsretning.

Her kan det være hensiktsmessig å lage en oppstilling i et regneark der samlet vekt og vektmoment beregnes: 

| Item      | Vekt [t] | LCG [m] | Moment [tm] |
| --------- | -------- | ------- | ----------- |
| Lettskip  | 1250     | 55      | 68750       |
| Last      | 500      | 70      | 35000       |
| Ferskvann | 150      | 12      | 1800        |
| ∑ sum     | 1900     | ???     | 105550      |

$$ 
LCG_{lastkondisjon} = \frac{Moment}{Vekt} 
$$

$$ 
LCG_{lastkondisjon} = \frac{105550[tm]}{1900[t]} 
$$

$$ 
LCG_{lastkondisjon} = 55.55[m] 
$$

```

## Vekts- og tyngdepunktsestimering
Å etablere anslag på vekt av *lettskip* og *dødvekt* i et tidlig designstadie er essensielt da det vil styre valg av fartøyets *hoveddimensjoner* i svært stor grad. Ofte blir det brukt referanseskip og/eller statistikk for å komme fram til et første estimat som en kan bruke i tidlig prosjektering. Ettersom designet utvikler seg vil en gjennomføre mer nøyaktige vektberegninger (_iterasjoner_). I byggeprosessen er det mulig å veie de ulike byggeblokkene før de sveises sammen. 

Vi har at et fartøys *initalstabilitet* er gitt ved $ GM_0 = KM-KG $. Plasseringen av tyngdepunktet *G* i høyde over kjølen *K* er derfor også viktig å estimere med rimelig grad av nøyaktighet.

## Øving i Jupyter Notebook 

{download}`Last ned øvingsoppgaver som omhandler vekt og tyngdepunkt i jupyter notebook <https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/lastekondisjoner/tyngdepunkt.ipynb">`
 

### Krengeprøve
Når et fartøy sjøsettes kan en bruke [Archimedes' prinsipp](https://en.wikipedia.org/wiki/Archimedes%27_principle) til å bestemme deplasementet. Tyngdepunktsplasseringen $VCG$ kan bestemmes med rimelig nøyaktighet ved å gjennomføre en *krengeprøve*. 


På større offshoreprosjekter der kapasitet av understell krever operatørene ofte at alle større vekter veies før de monteres ombord. Dette sørger for et eksakt vektsregnskap.



