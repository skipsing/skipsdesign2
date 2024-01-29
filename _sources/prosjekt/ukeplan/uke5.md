
## Uke 5 IMO intaktstabilitet og Maxsurf


### Status

- [x] Etablere første forslag til hoveddimensjoner basert på rederikrav 
- [x] Etablere et forslag til General Arrangement i Autocad (på blokknivå)
- [x] Etablere vektsberegning med tilhørene $Lcg$ og $Vcg$ for lastekondisjonen
- [x] Etablere preliminært skrog i Maxsurf med hensyn til hoveddimensjonene som foreslått
- [x] Kontrollere trim i lastekondisjonen basert på $Lcg$ og $Lcb$ funnet over. 
- [x] Justere arrangement av lasten (endrer $Lcg$)
- [x] Justere skrogform (endrer $Lcb$)
- [ ] Etablere lastekondisjonen i Maxsurf
- [ ] Kontrollere intaktstabilitet i Maxsurf 
- [ ] Selvstudium kapittel 8 "Intact Stability Regulations I" i Ship Hydrostatics boka (ikke kapittel 8.3 - 8.5)

Se Maxsurf Tutorial 3-8 som er lagt ut i blackboard. 

### Definisjon av lettskip og lastekondisjon i Maxsurf

I Maxsurf Stability skal det defineres lettskipsvekt og en lastekondisjon med maks last i henhold til arrangementet som er laget i Autocad. 

### Definisjon av tanker i Maxsurf
Det skal defineres to tanker:
- en *forpeak*tank forenfor kollisjonskottet i hele skipets høyde 
- en *akterpeak*tank. Denne kan være 4 eller 8 spant lang målt fra hekken.  

### Kontroller dypgang og trim 
Hvordan stemmer dypgang og trim i Maxsurf mot overslagsberegningene? Her er det vanskelig å få $C_B$ helt nøyaktig, og avvik vil forekomme. Forsøk å oppnå null trim ved hjelp av å omorganisere lastearrangementet (flytte $Lcg$). Eventuelt fylle noe ballast i forpeak eller akterpeak tankene. Her kan *enhetstrimmomentet* $MCT$ brukes til å beregne mengden ballastvann som må fylles for å oppnå null trim.  

### Kontroller IMO intaktstabilitet 
Kontroller om fartøyet møter stabilitetskriteriene til IMO. 
Her blir man utfordret i valget av hoveddimensjoner og plassering av lastarrangementet. 

### Vindkriterie 
Vindkriteriet er avhengig av måling av projisert areal over vannlinjen sett i *profilet*. Bruk Autocad til å måle arealet (AREA funksjonen) og legg dette inn under stabilitetskriteriet til IMO. 
Her blir man igjen utfordret på plassering av lastarrangementet. 





