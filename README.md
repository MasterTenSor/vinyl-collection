# Vinyl Collection (offline zoek-app)

# Handleiding

## Snel starten

Op een beurs zoek je een plaat in drie stappen:

1. Typ in de zoekbalk onderaan een stuk van de artiest, de titel of een tracknaam.
2. Kijk naar het icoon rechts van het resultaat: **lichtblauw gevuld** = in je collectie, **amber omlijnd** = op je wantlist, **lichtblauw met oranje stip** = in allebei.
3. Staat de plaat er niet bij? Tik dan op **D**, **S** of **Y** om verder te zoeken op Discogs, Spotify of YouTube.

Zoeken werkt zonder internet. Alleen de knoppen D, S en Y en het icoon (Discogs openen) hebben internet nodig.

## Zoeken

- Je lijst past zich aan terwijl je typt. Er wordt gezocht in artiest, titel en **alle tracks**, dus ook de B-kanten.
- Met meerdere woorden moeten alle woorden voorkomen in de artiest en titel van de plaat, of in de artiest, titel en één track. De volgorde maakt niet uit. Hoofdletters, accenten en "&" tegenover "and" maken niet uit.
- Kleine typfouten worden vergeven, maar alleen als er geen exacte treffers zijn. Zo blijft de lijst kort.
- Bovenaan kies je **Collection**, **Wantlist** of **Both**.
- De teller onder de knoppen toont "272 tracks · 34 records": het aantal gevonden tracks en het aantal platen.
- Bij heel veel treffers toont de app de eerste 80 platen. Typ meer letters of woorden om te verfijnen.

### De drie blokken

Zijn er verschillende soorten treffers, dan staat de lijst in blokken met een kopje:

- **Exact match:** de artiest of titel is precies je zoekterm (zoek je "change", dan staat de groep Change hier).
- **In artist or title:** de artiest of titel bevat je zoekterm.
- **In track titles only:** alleen een track bevat je zoekterm.

Is er maar één soort treffer, dan staat er geen kopje.

## Resultaten lezen

- Elke plaat is één kaart: titel, artiest, tracks en rechts het icoon.
- **Icoon:** het type (7 inch single, 10 of 12 inch maxi-single, album, compilatie, cd, single-cd of overig) en de kleur. Zie de legende hierboven.
- **7 inch en 12 inch** tonen altijd alle tracks.
- **Albums, compilaties en cd's** zijn ingeklapt en tonen alleen de tracks die bij je zoekopdracht passen. Met "All N tracks ▾" klap je de hele tracklist uit. Zie je geen tracks, dan staat de zoekterm niet als track op die plaat.
- Matcht alleen een track, dan zie je de eerste vier treffers. Uitklappen toont de hele tracklist met de treffers in vet.
- Bij een compilatie staat achter elke track de eigen artiest.
- Een **Note** onder een plaat is je eigen notitie uit de wantlist.
- Staat er achter de artiest een mapnaam, dan zit de plaat in een map die niet meedoet aan het zoeken. Zie "Bijwerken".
- Tik op het **icoon** om die plaat in de Discogs-app te openen.

## Knoppen en meldingen

- **Offline-pil** linksboven: groen = alles staat in de app en werkt zonder internet. Rood met een percentage = de tracklists worden nog opgehaald. Tik erop voor de voortgang.
- **Aantal records** en daarnaast het **versienummer** (bv. v1.13).
- **?** opent deze uitleg, **↻** opent Update.
- **D, S, Y** bovenaan: zoeken op wat je getypt hebt in Discogs, Spotify of YouTube.
- **Tik op een gevonden track:** er verschijnen D, S en Y onder die track, met artiest en tracktitel als zoekterm. Nog eens tikken sluit het menu weer.
- **"+N records in inactive folders":** treffers uit mappen die niet meedoen aan het zoeken. Tik om ze toe te voegen.
- **No hits:** staat er niets, dan staan er drie grote knoppen om op Discogs, Spotify of YouTube verder te zoeken.

## Bijwerken

1. Exporteer in Discogs je collectie en je wantlist als CSV en bewaar ze op Google Drive.
2. Tik op **↻** en kies bij Update de twee bestanden via de Files-app.
3. Controleer de mappen en tik op **Update and fetch new tracklists**.

- **Update** voegt toe en past aan. **New collection** begint met een lege database, bv. als je helemaal opnieuw wil. Dat vraagt twee keer tikken om te bevestigen.
- **Mappen:** bij "In app" bepaal je welke mappen in de app komen, bij "In search" welke meedoen aan het zoeken. Nieuwe mappen krijgen het label "New". Verdwenen mappen worden gemeld.
- Alleen **nieuwe platen** halen een tracklist op. Laat de app open staan en het scherm aan tot de pil groen is.
- Wordt het opgehalen onderbroken, open de app dan opnieuw. Tik op **Resume** om precies verder te gaan.
- Een **Discogs-token** (optioneel) maakt het ophalen veel sneller (60 in plaats van 25 aanvragen per minuut). Plak hem op het Update-scherm, tik op **Test** en dan op **Save**.
- **Check a release** onderaan op Update toont wat de app van één release bewaard heeft.

## Problemen oplossen

- **De app toont een oude versie:** upload de nieuwe bestanden en open de app twee keer. Controleer het versienummer rechtsboven.
- **Een track vind ik niet:** zolang de pil rood is, ontbreken tracklists. Wacht tot de pil groen is, of tik op Resume.
- **Spotify of YouTube opent in Safari:** meld het, dan zoeken we een andere link.
- **Discogs opent in een mini-browser:** de zoek-knop D kan de Discogs-app niet openen. Het icoon bij een plaat wel.
- **Verwijder de app niet van je beginscherm:** de database staat alleen in die app en is dan weg. Dan moet je alles opnieuw importeren.

# Installatie

## Wat zit erin
- `index.html`: de hele app
- `sw.js`: zorgt dat de app offline opent
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`: voor "Zet op beginscherm"

Alle bestanden moeten samen in dezelfde map staan.

## Installeren (eenmalig, via GitHub Pages)
De app moet via https draaien, anders werkt offline niet. GitHub Pages is hiervoor het eenvoudigst.

1. Ga op github.com naar **New repository**, noem het bv. `vinyl-collection`, zet het op **Public**, klik **Create repository**.
2. Klik **uploading an existing file** en sleep ALLE bestanden uit deze map erin (niet de map zelf). Klik **Commit changes**.
3. Ga naar **Settings → Pages**. Kies bij *Source* **Deploy from a branch**, branch **main**, map **/ (root)**, en klik **Save**.
4. Na 1 à 2 minuten staat de app op `https://MasterTensor.github.io/vinyl-collection/`.
5. Open die link in **Safari op je iPhone** (met internet). Tik op **Delen → Zet op beginscherm**.
6. Open de app vanaf het beginscherm. Tik rechtsboven op het vernieuw-icoon (**Update**).
7. Kies de twee CSV's via de Files-app (Google Drive), controleer de mappen, en tik **Import and fetch tracklists**.
8. Laat de app open en het scherm aan tot de tracklists binnen zijn (ongeveer 70 minuten met token, 3 tot 3,5 uur zonder). Wordt het onderbroken, open dan de app opnieuw: er staat "Interrupted" met een **Resume**-knop.
9. Als de pil linksboven groen "Offline" toont, kun je alles zonder internet doorzoeken.

## Later bijwerken
Exporteer nieuwe CSV's uit Discogs, ga naar **Update**, kies de bestanden en tik op import. Alleen nieuwe records halen een tracklist op.

## Discogs-token (optioneel)
Plak je personal access token op het Update-scherm en tik op **Test** om te controleren of hij werkt; daarna **Save**. Met token 60 aanvragen per minuut, zonder 25.

## Belangrijk: verwijder de app niet
Op iPhone heeft de app op het beginscherm een eigen, aparte opslag (los van Safari). Verwijder je de app, dan is de database weg. Een nieuwe versie van de app komt vanzelf binnen: upload de nieuwe bestanden en open de app twee keer. Rechtsboven in het zoekscherm staat het versienummer (nu v1.13).
