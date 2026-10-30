# Goedgekeurde claims

Alleen wat hier staat mag de motor in berichten beweren. Heeft een concept een claim nodig die hier niet staat, dan gaat het naar Robbert. Nieuwe claims komen er alleen bij na akkoord van Robbert, met bron.

Bron van waarheid voor prijzen en pakketten: `occasly-site/src/lib/packages.ts`. Haal bedragen altijd daar vandaan, nooit uit dit bestand of uit je geheugen.

## Werkwijze en koppeling

| Claim | Bron |
|---|---|
| Je blijft je auto's invoeren in je eigen voorraadsysteem, zoals je gewend bent. | `systems.ts` |
| Nieuwe auto erin? Automatisch online. Verkocht? Automatisch eraf. | `systems.ts` |
| Werkt met VWE, Autoflex, UCC, AutoData Wheelerdelta en vrijwel elk ander Nederlands systeem. | `site.ts` (`INVENTORY_SYSTEMS`), homepage |
| Je vraagt de koppeling aan bij je leverancier; wij sturen je de tekst mee en doen de rest. | `systems.ts` |
| Reken op enkele werkdagen doorlooptijd; het technische deel doen wij binnen een dag. | `systems.ts` (`CONNECT_LEAD_TIME`) |
| Stap je later over naar een ander voorraadsysteem, dan hoeft je site niet opnieuw gebouwd te worden. | `systems.ts` |
| Zonder voorraadsysteem: één keer invoeren bij ons en de auto staat op je eigen site én op Marktplaats en AutoScout24. | `packages.ts` (`VMS_MODULE`) |

## De site

| Claim | Bron |
|---|---|
| Je eigen domein, in je eigen huisstijl. | `packages.ts` (`BASE_FEATURES`) |
| Voertuigpagina's met foto's en alle specificaties. | `packages.ts` |
| Bellen en WhatsApp vanaf elke occasion. | `packages.ts` |
| Je site laadt onder 1 seconde. | homepage (`HERO_STATS`) |
| Hosting, beveiliging, back-ups en onderhoud zitten in het abonnement. | `packages.ts` (`ALWAYS_INCLUDED`) |
| Verkoper en Dealer Pro: proefrit-, bod- en inruilaanvragen, inruil met kentekencheck, financial lease op de voertuigpagina. | `packages.ts` |
| Aanvragen komen per mail binnen en waar mogelijk ook terug in je eigen systeem. | `systems.ts` |

## Prijs en voorwaarden

| Claim | Bron |
|---|---|
| Vast bedrag per maand plus een eenmalige opstartprijs, per pakket. Bedragen uit `PACKAGES`. Alle prijzen exclusief btw. | `packages.ts` |
| Je betaalt niet per auto. | `packages.ts` (`STOCK_NOTE`) |
| Kanaaltarief van Hexon betaal je via je voorraadleverancier; verschilt per leverancier. | `packages.ts` (`PRICING_NOTES.hexonFee`) |
| Marktplaats en AutoScout24 sluit je zelf af en betaal je rechtstreeks aan het portaal. | `packages.ts` (`PRICING_NOTES.portalFee`) |
| Het is een abonnement. Je domein, je content en je leads blijven van jou en kun je meenemen. | `AGENTS.md` (occasly-site) |

## Persoonlijk

| Claim | Bron |
|---|---|
| Eén vast aanspreekpunt: Robbert Vos, te bellen of appen op 06 52 10 38 37. | `site.ts` |
| Bekijk een voorbeeld: demo.occasly.nl (fictief demobedrijf). | `site.ts` (`demos`) |

## Nooit beweren

- Dat de website eigendom wordt of is van de dealer.
- "Maatwerk" of "uniek ontwerp" bij Etalage of Verkoper. Alleen Dealer Pro is maatwerk; de opstartprijs daar is een vanaf-prijs en meertaligheid is een mogelijkheid, niet inbegrepen.
- Een eigen prijs voor de voorraadbeheermodule (nog niet vastgesteld).
- Klanten, klantcijfers, reviews of resultaten (er zijn nog geen klanten).
- Kortingen, acties of deadlines. Prijsafspraken doet alleen Robbert.
- "Binnenkort", "testfase" of "wachtlijst" over het voorraadbeheer met doorplaatsing.
- Iets over een concurrent.
- Een meting over hun site die de motor niet zelf heeft gedaan (met datum en bron in de wachtrij).
