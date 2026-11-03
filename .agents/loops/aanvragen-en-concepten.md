# Loop: aanvragen en concepten

| Onderdeel | Invulling |
|---|---|
| **Check cadence** | Werkdagen om 8, 10, 12, 14, 16 en 18 uur (Europe/Amsterdam). |
| **Acts when** | (a) Er staan aanvragen in `site_leads` die nieuwer zijn dan `Instellingen!B17`, of (b) er staan bedrijven in Prospects met Status "benaderen" zonder bijbehorend voorstel in de Wachtrij. Anders: niets doen, alleen een korte regel in Logboek. |
| **Purpose** | Elke aanvraag van occasly.nl en elk gekozen prospect binnen twee uur voorbereid in de Wachtrij, zodat Robbert alleen hoeft te kiezen. |
| **Skills used** | `lead-qualification`, `discovery`, `sales-presentations`, `cold-email`, `sales-copywriting`, `personalization-at-scale`, `objection-handling`. |
| **Loop body** | 1. Noodknop `Instellingen!B2` lezen; stop als niet `aan`. 2. Nieuwe aanvragen ophalen uit `site_leads` (`created_at` groter dan `B17`). Per aanvraag: site van het bedrijf zoeken en checken (zoals in de prospectlijst), een conceptantwoord van Robbert schrijven en een demobriefing van één scherm. Beide als één rij in de Wachtrij: Type "aanvraag", Kanaal "zelf mailen of bellen", Status "voorstel". 3. `B17` bijwerken naar de `created_at` van de nieuwste verwerkte aanvraag. 4. Per prospect met Status "benaderen" zonder Wachtrij-voorstel: een eerste mail volgens play 1 of 2 uit `outbound/plays.md` (met een zelf gemeten bevinding en datum) en een belbriefing. Twee rijen in de Wachtrij: Type "eerste mail" (Kanaal "mail via lemlist") en Type "belbriefing" (Kanaal "telefoon"), Status "voorstel". Zet in de Prospects-rij Status op "benaderd" pas nadat Robbert een voorstel op "akkoord" zette en het is uitgevoerd; deze loop zet hem niet zelf. |
| **Self-check** | Elke bewering staat in `outbound/claims.md`. Elke bevinding over hun site is vandaag zelf gemeten en heeft een bron-URL. Afmeldlijst gecheckt. Geen em-streepjes. |
| **State / idempotency** | `Instellingen!B17` = tijdstip van de laatst verwerkte aanvraag. Prospects: een voorstel bestaat al als er in de Wachtrij een rij is met dezelfde bedrijfsnaam en Type "eerste mail". |
| **Stop / bail-out** | Noodknop uit; Supabase of de sheet niet bereikbaar (loggen en stoppen); een aanvraag die op spam lijkt (geen bedrijf, onzin): niet uitwerken, wel loggen. |
| **Output** | Rijen in de Wachtrij, `B17` bijgewerkt, één regel in Logboek zonder persoonsgegevens. |

Deze loop verstuurt niets. Versturen gebeurt pas in de loop "wachtrij verwerken", die aangaat als het verzenddomein is opgewarmd.
