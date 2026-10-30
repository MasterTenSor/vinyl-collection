# Vinyl Collection (offline zoek-app)

## Wat zit erin
- `index.html` – de hele app
- `sw.js` – zorgt dat de app offline opent
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` – voor "Zet op beginscherm"

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
Plak je personal access token op het Update-scherm. Met token 60 aanvragen per minuut, zonder 25.

## Nog te testen op je iPhone
- Of een tik op het icoon het Discogs-app opent of Safari.
- Of de data bewaard blijft na dagen niet gebruiken (de app vraagt iOS om persistente opslag).

## Belangrijk: verwijder de app niet
Op iPhone heeft de app op het beginscherm een eigen, aparte opslag (los van Safari). Verwijder je de app, dan is de database weg. Een nieuwe versie van de app komt vanzelf binnen: upload de nieuwe bestanden en open de app twee keer. Rechtsboven in het zoekscherm staat het versienummer (nu v1.4).
