# Sjekk av IMO stabilitetskriterier 


<p style="text-align:center;">
    ✍️ Lars Erik Nygård  <a href="mailto:lars.e.nygard@ntnu.no">📧</a> 08.02.2024 📅 
</p>

-----


I denne økten skal vi anvende Python og Jupyter Notebook til å databehandle og kontrollere om skipet tilfredstiller IMO's krav til stabilitet.


```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/intakt-stabilitet/images/gz-kurve-variasjon.PNG
---
scale: 50 %
align: center
--- 
GZ-kurven er sterkt avhengig av skipets form og tyngdepunktsplassering vertikalt. Bildet hentet fra {cite}`havromsteknologi`. 
```

test {cite}`havromsteknologi`
test {cite}`shiphydrostatics`

## Stabilitetsanalyse i Maxsurf Stability 

Vi skal først bruke Maxsurf Stability til å generere og *logge* GZ verdien for lastekondisjonen som dere har satt opp. 

Vi må først justere litt på  innstillingene for hvordan Maxsurf skal *logge* dataene fra stabilitetsanalysen. Default innstillingene er å krenge båten fra -30 til 180 grader styrbord, og med inkrement på 10 grader. Vi ønsker litt mere nøyaktige data, men vi trenger bare å krenge båten fra 0 til ca 90 grader. 


Etter at vi har lastet inn prosjektet vårt i Maxsurf Stability Advanced velger vi fra toppmenyen: 
> Analysis > Heel 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/intakt-stabilitet/images/maxsurf-stability-range-step.PNG
---
scale: 50 %
align: center
--- 
Justering av range som Maxsurf skal krenge båten fra 0-90 grader, og med kalkulasjon for hver 1 grad krenging
```

Videre må vi spesifieres hva som skal logges av data: 
> Display > Data Format 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/intakt-stabilitet/images/maxsurf-stability-data.PNG
---
scale: 50 %
align: center
--- 
Data som skal logges er GZ verdi og presentasjonen skal være horisontal
```

Det må spesifiseres at det er store krengevinkler vi skal analysere: 

> Analysis Mode: Large Angle Stability 

så velger vi hvilken lastekondisjon vi skal analysere, og videre *intact*kondisjon. Så er det bare å kjøre analysen med grønn pil. 

```{figure} https://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/intakt-stabilitet/images/maxsurf-stability-large-angle-stability-setting.PNG
---
scale: 50 %
align: center
--- 
Analysemodus *Large angle stability* med valgt lastkondisjon (du kan ha gitt denne et annet navn) og lastetilstand skal stå på *intact*
```
Dette tar litt tid så vent til programmet har kjørt seg ferdig.  Vi kan inspisere reusultatene fra analysen ved å: 

> Window > Results > Large Angle stability 

Vi får da opp en tabell som viser resultatene som er beregnet for hvert steg i analysen. *Loggen* fra analysen må vi så lagre i en egen fil. 

> File > Save Stability Results As 

I dialogboksen så gir vi filen et navn og lagrer den på et egnet sted (på hjemmeområdet). Denne har filendelsen *.txt* og kan åpnes i enkle tekstprogram slik som *Notepad* og *Textpad*.

## Analyse av data i Jupyter Notebook 

Jupyter Notebooken lastes ned herfra: 

<a href="http://cdn.jsdelivr.net/gh/skipsing/skipsdesign2/intakt-stabilitet/images/stab_analyse.zip" download>📥 Download</a> 

Dette er en .zip fil som inneholder:
- jupyter notebooken
- eksempelfil.txt (gzdata eksempel)
- et plot generert fra jupyter notebooken

```{admonition} Filplassering
:class: caution

Filen med dataene må ligge i samme mappe som jupyter notebooken for at den skal kunne leses! 
```







