# Bedankt-label — overdracht

**Wat het is:** één HTML-bestand dat in de browser draait. Je sleept er een QR-code in,
kiest de breedte, en print op een Brother DK-11241 label (102 x 152 mm).
Geen server, geen installatie, geen sleutels of wachtwoorden.

## Online
- Link: https://peterhoman.github.io/bedankt-label/
- Repo: https://github.com/peterhoman/bedankt-label (openbaar — moet, anders werkt de gratis link niet)
- Draait via GitHub Pages vanaf branch `main`, map `/ (root)`

## Bestanden
| bestand | wat |
|---|---|
| `index.html` | wat online staat — kopie van het bestand hieronder |
| `bedankt-label-102x152-DK11241.html` | het origineel, met de nette naam |
| `bedankt-label-102x152-DK11241_1.html` | oudere versie, staat NIET op GitHub (zie .gitignore) |

## Iets aanpassen en online zetten
Pas `bedankt-label-102x152-DK11241.html` aan, dan:

```bash
cp bedankt-label-102x152-DK11241.html index.html
git add -A && git commit -m "wat je hebt veranderd" && git push
```

Na een minuutje staat het op de link. Controleren:

```bash
curl -s -o /dev/null -w "%{http_code}\n" https://peterhoman.github.io/bedankt-label/
```

`200` = goed.

## Achtergrond
Deze map had geen eigen git-repo en viel onder de repo van een ander project
(`avantius-sync-feed-B-living`, één map hoger). Op 29 augustus 2026 is hier
`git init` gedaan zodat deze map zelfstandig is. De `.git` één map hoger blijft
staan — die is van dat andere project, niet opruimen.

## Stand van zaken
- 30 aug 2026: labeltekst aangepast naar "Klein bedrijf, maar blij met elke review".
  Tekst is nu 4 regels. Past op de standaard QR-breedte (44 mm); op het maximum
  (62 mm) valt het onderste hartje 0,6 mm weg. Peter vond dat goed zo — niet aanpassen.
- Niets open.

## Berichten aan andere chats
Altijd met SendMessage, met als `to` het nummer van de chat (`local_…`, via
list_sessions) — niet de naam. Via het nummer wordt een stilstaande chat wakker;
via de naam blijft het bericht liggen. Een gewekte chat voert niets door, zet niets
op GitHub en verandert geen instellingen zonder Peters ja. (Staat ook in de
algemene CLAUDE.md, regel van 27-10-2026.)
