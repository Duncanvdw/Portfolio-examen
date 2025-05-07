# **Test Software**
---
## Testplan
## Doel van de test
Het doel van deze test is de functionaliteit, user stories en de responsiviteit te testen. Dit testplan bevat de testcases voor de website die ik heb gemaakt.

## Onderwerpen van de tests
 1. **US-03**: Als (mobiele) bezoeker wil ik dat de website er strak uitziet en goed functioneert op mijn smartphone
 2. **US-04**: Als bezoeker wil ik dat de website snel laadt, ongeacht het apparaat
 3. **US-05**: Als beheerder wil ik dat de inhoud van de website duidelijk en gemakkelijk kan worden aangepast en toegevoegd wanneer dat nodig is

---

# Test cases


## **Case 1 - Responsiviteit**
### Hoofdscenario
1. **Test scenario**: Als ik het formaat van het apparaat waarop ik de website bekijk verander, blijft alles er netjes uitzien.
2. **Stappen**: Inspecteer de pagina, klik op toggle device toolbar, zet hem op responsive en verander aan de rechterkant van de pagina het formaat van de website.
3. **Test data**: Een pagina met informatie erin.
4. **Verwachte uitkomst**: Als de website van formaat veranderd wordt, blijft alle informatie in verhouding en valt niks buiten de bestemde plaatsen of buiten het scherm.
5. **Resultaat**: 

### Alternatief scenario 1
1. **Test scenario**: Als ik de website bekijk op een mobiel apparaat.
2. **Stappen**: Open de website via de browser van een mobiel apparaat of simuleer een mobiel scherm in de developer tools.
3. **Test data**: Een pagina met tekst en afbeeldingen.
4. **Verwachte uitkomst**: De content schaalt correct, navigatie blijft bruikbaar en tekst is leesbaar zonder horizontaal te scrollen.
5. **Resultaat**: 

### Alternatief scenario 2
1. **Test scenario**: Als ik de website bekijk op een groot scherm.
2. **Stappen**: Open de website op een scherm met een resolutie van 3840x2160 of simuleer dit formaat via developer tools.
3. **Test data**: Pagina's met veel layout-elementen.
4. **Verwachte uitkomst**: De layout schaalt naar een bredere weergave zonder dat elementen overdreven veel witruimte bevatten of uitrekken.
5. **Resultaat**: 

### Conclusie

---

## **Case 2 - Snelle laadtijden**
### Hoofdscenario
1. **Test scenario**: Als je een pagina binnen de website inlaadt, wordt de pagina snel weergegeven.
2. **Stappen**: Open de pagina in een browser en meet de laadtijd met Lighthouse.
3. **Test data**: Een pagina met een video of grote foto.
4. **Verwachte uitkomst**: De pagina wordt snel ingeladen en Lighthouse geeft een hoog performance resultaat.
5. **Resultaat**: [resultaatHoofdscenario2](images/hoofd-scenario-2-snel-laden.png) Zoals je ziet is het resultaat niet zo goed als de verwachting, de score die is terug gekomen is een 87. Dit is niet slecht maar ook niet super goed.

### Alternatief scenario 1
1. **Test scenario**: Als de gebruiker de website opent met een trage internetverbinding.
2. **Stappen**: Simuleer een trage 3G-verbinding via developer tools en laad de pagina.
3. **Test data**: Pagina met afbeeldingen of video.
4. **Verwachte uitkomst**: De pagina blijft functioneel en toont ten minste een laadbalk of skeleton loader; grote assets worden vertraagd maar niet geblokkeerd.
5. **Resultaat**: [alternatiefscenario2.1](images/alternatief-scenario-2-1-snel-laden.png) Zoals je ziet, word de pagina binnen 10 seconden geladen. Na 2 seconden was de pagina al bruikbaar en na 10 seconden was alles ingeladen behalve de video die aan de onderkant van de screenshot ziet, deze was na 15 seconden ingeladen.

### Alternatief scenario 2
1. **Test scenario**: Als de browser cache is geleegd.
2. **Stappen**: Leeg de cache van de browser en laad vervolgens een pagina.
3. **Test data**: Pagina met standaard content.
4. **Verwachte uitkomst**: Pagina laadt nog steeds binnen acceptabele tijd, zonder afhankelijk te zijn van cache.
5. **Resultaat**: [alternatiefscenario2.1](images/alternatief-scenario-2-2-snel-laden.png) Zoals je ziet, word bijna de hele pagina binnen 4 seconden ingeladen, na 2 seconden kon je er al doorheen scrollen en was de website bruikbaar. Na de 4 seconden werden er nog een paar dingen op de achtergrond ingeladen waar je geen last van hebt tijdens het scrollen.

---

## **Case 3 - Makkelijk toevoegen en aanpassen inhoud**
### Hoofdscenario
1. **Test scenario**: De gebruiker verandert of voegt nieuwe informatie toe aan de website via het CMS.
2. **Stappen**: Login op het CMS, navigeer naar de pagina, wijzig of voeg nieuwe content toe, en sla op.
3. **Test data**: De pagina die veranderd moet worden en het CMS waarin je tekstvelden in kan vullen.
4. **Verwachte uitkomst**: De inhoud van de pagina moet veranderd of toegevoegd zijn op de live site.
5. **Resultaat**: 

### Alternatief scenario 1
1. **Test scenario**: De gebruiker probeert een leeg veld op te slaan.
2. **Stappen**: Open een pagina in het CMS, verwijder alle tekst uit een vereist veld (zoals titel of inhoud), en klik op "Opslaan".
3. **Test data**: Een veld zonder inhoud.
4. **Verwachte uitkomst**: Het CMS toont een foutmelding of markeert het lege veld als verplicht; de wijziging wordt niet opgeslagen.
5. **Resultaat**: 

### Alternatief scenario 2
1. **Test scenario**: De gebruiker voert ongeldige HTML of scriptcode in het CMS in.
2. **Stappen**: Voeg een `<script>`-tag of andere niet toegestane HTML in een inhoudsveld in via het CMS.
3. **Test data**: `<script>alert("test")</script>` of vergelijkbare code.
4. **Verwachte uitkomst**: Het CMS voorkomt het opslaan van de ongeldige input of filtert de code automatisch uit bij opslaan.
5. **Resultaat**: