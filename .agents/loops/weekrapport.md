# Loop: weekrapport

| Onderdeel | Invulling |
|---|---|
| **Check cadence** | Maandag 07:51 (Europe/Amsterdam). |
| **Acts when** | Altijd; een week zonder activiteit is ook informatie. |
| **Purpose** | Robbert in één scherm laten zien wat de motor deed en wat er van hem nodig is. |
| **Skills used** | `marketing-loops` (weekly-marketing-review), `revops`, `analytics`. |
| **Loop body** | 1. Noodknop lezen. 2. Tellen over de afgelopen 7 dagen: nieuwe prospects per tier en regio; statuswijzigingen in Prospects; Wachtrij per status; aanvragen in `site_leads`; afmeldingen. 3. PageSpeed mobiel van occasly.nl meten. 4. Als `OCCASLY_LEMLIST_API_KEY` werkt: status van campagnes en verzonden mails. 5. Rapport schrijven in het format hieronder. |
| **Self-check** | Alle getallen komen uit de sheet, Supabase of een meting van vandaag. Geen schattingen. |
| **State / idempotency** | Eén rapport per week; staat er deze week al een weekrapport in Logboek, dan niets doen. |
| **Stop / bail-out** | Noodknop uit; sheet niet bereikbaar. |
| **Output** | Eén regel in Logboek (Loop "weekrapport", Details = het rapport) en het rapport als laatste bericht van de run. |

## Format

```
Week van [datum]
Prospects: [n] nieuw ([tier 1/2/3]), regio [naam]. Gekozen om te benaderen: [n].
Wachtrij: [n] voorstel, [n] akkoord, [n] uitgevoerd, [n] afgewezen.
Aanvragen via occasly.nl: [n]. Snelheid occasly.nl mobiel: [score].
Mail: [status lemlist of "nog niet actief"].
Nodig van jou (max. 3): [...]
```
