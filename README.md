# MealPlan PWA — Fase 7

Dit is een aparte, gratis webapp-versie van MealPlan. De bestaande Swift-app blijft ongewijzigd.

## Wat zit erin
- Recepten + ingrediënten
- Manuele planning 1–14 dagen
- Nederlandse weekdagen
- Automatische boodschappenlijst
- 'In huis'
- Lokale ideeën
- Delen van planning en boodschappen
- Volledige JSON back-up en herstel
- Offline app-shell via Service Worker
- PWA manifest voor installatie op iPhone

## Belangrijk
Een PWA moet via HTTPS (of localhost tijdens ontwikkeling) worden geopend. Je kunt index.html dus niet simpelweg vanuit Bestanden openen en verwachten dat installatie/offline caching werkt.

## Publiceren
Upload deze volledige map ongewijzigd naar een HTTPS webhost (bijvoorbeeld GitHub Pages, Cloudflare Pages of Netlify). Open daarna de HTTPS-link in Safari op de iPhone en kies:
Deel > Zet op beginscherm > Open als webapp.

## Data
De data staat lokaal in de browseropslag van die iPhone. Maak daarom geregeld:
Instellingen > Exporteer volledige back-up
en bewaar het JSON-bestand in Bestanden/iCloud Drive.

## Migratie
De SwiftData-database uit de native app wordt niet automatisch door Safari gelezen. Bestaande native recepten moeten dus apart worden gemigreerd. Deze PWA heeft daarvoor JSON-import; een latere native-export kan hetzelfde JSON-formaat produceren.
