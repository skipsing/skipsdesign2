# IMO vindkriterie 

-----

<p style="text-align:center;">
    ✍️ Lars Erik Nygård  <a href="mailto:lars.e.nygard@ntnu.no">📧</a> 12.02.2024 📅 
</p>

-----

## Læringsutbytte
- Forstå hva IMO vindkriterie er
- Kunne beskrive hva IMO vindkriteriet går ut på 
- Kunne beregne og gjøre vurderinger av input som er nødvendig
- Kunne anvende og kontrollere IMO vindkriteriet i praksis på eget prosjekt
- Gjøre vurderinger på tiltak om kriteriet ikke er tilfredstilt 

## Introduksjon

I tillegg til de generelle kravene som vi så på tidligere har IMO også et *vindkriterie*. De generelle kravene er kun basert på skrogets form og tyngdepunktsplassering, mens vindkriteriet også ser på hvor stort areal som er eksponert for vind. Bakgrunnen for dette kriteriet er at en betrakter fartøyet som *dødt*, det vil si at det har mistet motorkraft og muligheten til å navigere. Fartøyet vil da kunne legge seg på siden og få både vind og bølger fra minst gunstige retning samtidig. En kan finne mere informasjon om dette kriteriet [på IMO sine nettsider](https://www.imorules.com/GUID-8206CA1C-E079-4E62-BF3F-9BECF96D6969.html). 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/intakt-stabilitet/images/IMO-severe-wind-curve.PNG
---
scale: 50 %
align: center
--- 
IMO vindkriterie
```

## 3 samtidig virkende krefter

Kriteriet ser på 3 effekter som inntreffer samtidig. 

- Konstant vind som forårsaker krengende arm $l_{w1}$
- bølger fra siden som forårsaker krenging med vinkelen $ \phi_1 $
- Vindkast som forårsaker krengende arm $l_{w2}$

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/intakt-stabilitet/images/imo-weather-situations.PNG
---
scale: 50 %
align: center
--- 
krenging pga konstant vind, bølge og vindkast
```

## Akseptkriterie 

Kriteriet ser på energibalansen i det fartøyet svinger med vinden. Energien representert i "b" må være større enn energien lagret i "a" på grunn av konstant vind, bølge og vindkast. 

$$ \text{Areal "b" } \geq \text{ Areal "a" }$$

En ser av grafen at arealet til "b" kuttes ved $\phi_2$ og der denne vinkelen er det minste av 50grader og vinkelen ved første vanninntrenging (downflooding). 

## Beregning

Krengende arm, $l_{w1}$, for den konstante vinden er gitt som

$$ l_{w1} = \frac{P \times A \times Z}{1000 \times g \times \Delta} $$

og der hvor 

$$ P = 504 \frac{N}{m²} $$

$$ A = \text{ Projisert areal av fartøy og last over vannlinjen i }m² $$

$$ Z = \text{ Vertikal avstand mellom arealsenteret til A og halve dypgangen T i m} $$

$$ g = 9.81\frac{m}{s²} \text{(gravitasjonskonstant) }  $$

$$ \Delta = \text{vektsdeplasementet i t } $$

Krengende arm, $l_{w2}$, for vindkast er gitt som

$$ l_{w2} = l_{w1} \times 1.5 $$


## Arealberegning i Autocad 

Vi skal beregne det projiserte arealet i Autocad. Først kan den være lurt å tegne en polyline som omslutter profilet. (starter og stopper i samme punkt)

> PL 

Med et lukket areal kan areal og arealsenter beregnes. Funksjonen for det er 

> MASSPROP 

Først må arealet defineres som en region

> REGION

Her er vi ute etter areal (Area) og avstand fra arealsenter til vannlinjen (differansen mellom Bounding box Y og Centroid)


