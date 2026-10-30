# Loop: prospectlijst

| Onderdeel | Invulling |
|---|---|
| **Check cadence** | Wekelijks, maandag 07:00 (Europe/Amsterdam). |
| **Acts when** | Er zijn in de huidige regio bedrijven met erkenning Bedrijfsvoorraad die nog niet in de Prospects-tab staan, of waarvan de check ouder is dan 90 dagen. Anders: niets doen en "geen nieuwe bedrijven" loggen. |
| **Purpose** | Elke week tot 50 gescoorde bedrijven met een echte, gemeten aanleiding klaarzetten. |
| **Skills used** | `prospecting` (local SMB), `ideal-customer-profile-matching`, `prospect-research-integration`, `data-enrichment-integration`, `trigger-event-detection`, `seo-audit`. |
| **Loop body** | 1. Lees `Instellingen!B2`; stop als het niet `aan` is. 2. Haal de RDW-bedrijven van de regio op (zie `outbound/brief.md`). 3. Filter de anti-persona weg op naam. 4. Zoek per bedrijf de eigen website; laad homepage en voorraadpagina. 5. Leg vast: voorraadweergave, signalen van voorraadsysteem of leverancier, aantal auto's, mobiele basis, PageSpeed-score mobiel (zodra er een sleutel is), rechtsvorm, algemeen mailadres, Marktplaats/AutoScout24. 6. Score 0 tot 100 volgens de tabel hieronder. 7. Schrijf nieuwe of bijgewerkte rijen in de Prospects-tab. |
| **Self-check** | Elke bevinding heeft een bron-URL en een datum. Geen URL gebruiken die niet geladen is. Bij twijfel: "onbekend", geen gok. |
| **State / idempotency** | Sleutel: RDW-volgnummer. Een bedrijf wordt niet opnieuw gecheckt binnen 90 dagen. Laatste run in `Logboek`. |
| **Stop / bail-out** | Noodknop uit; RDW-API niet bereikbaar (loggen, volgende week opnieuw); meer dan 20 procent van de sites onbereikbaar (loggen en stoppen, waarschijnlijk een netwerkprobleem). |
| **Output** | Rijen in de Prospects-tab, een regel in Logboek, en in het weekrapport het aantal nieuwe prospects per tier. |

## Score

| Signaal | Punten |
|---|---|
| Verkoopt occasions aan consumenten (zichtbaar op site of portaal) | +30 |
| Voorraad 5 tot 150 auto's | +15 |
| Voorraad in een kader van een leverancier, of geen eigen pagina per auto | +20 |
| Geen eigen site, wel occasions op een portaal | +20 |
| Site verouderd (copyright ouder dan 3 jaar, geen viewport, geen https) | +10 |
| Geen bel- of WhatsAppknop op mobiel | +5 |
| Werkt met een voorraadsysteem dat Occasly koppelt | +10 |
| Nieuw bedrijf (nieuwe erkenning in de laatste 90 dagen) | +10 |
| Merkdealer van een groep, export/groothandel, geen occasions | uitsluiten |

Tier 1: 70 of hoger. Tier 2: 50 tot 69. Tier 3: 30 tot 49. Onder 30: overslaan.
