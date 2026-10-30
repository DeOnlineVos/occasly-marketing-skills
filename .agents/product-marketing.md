# Product Marketing Context

**Document version:** v1
**Last updated:** 2026-10-30
**Bron van waarheid:** `occasly-site` (`src/lib/packages.ts`, `src/lib/site.ts`, `src/lib/systems.ts`) en `docs/masterplan.md`. Wijkt dit document daarvan af, dan wint de code. Prijzen en pakketinhoud nooit uit je hoofd gebruiken: altijd uit `packages.ts`.

## Changelog

- v1 (2026-10-30): eerste versie, opgesteld uit de site-code en het masterplan.

## Product Overview

**One-liner:** Je eigen autowebsite zonder dubbel werk: je blijft je occasions beheren in je eigen voorraadsysteem, Occasly zet ze automatisch op je eigen website in jouw huisstijl.
**What it does:** Occasly bouwt en beheert websites voor autobedrijven. De voorraad komt automatisch uit het voorraadsysteem dat de dealer al gebruikt (VWE, Autoflex, UCC, AutoData Wheelerdelta en andere, via Hexon). Nieuwe auto erin, dan automatisch online; verkocht, dan automatisch eraf. Aanvragen (proefrit, bod, inruil) komen per mail binnen en waar mogelijk terug in het eigen systeem.
**Zonder voorraadsysteem:** dealers die geen voorraadsysteem hebben, kunnen het voorraadbeheer met doorplaatsing van Occasly gebruiken: één keer invoeren, en de auto staat op de eigen site en op Marktplaats en AutoScout24. Dit wordt als beschikbaar verkocht. De eigen moduleprijs van Occasly is nog niet vastgesteld en mag nergens genoemd worden; de Hexon-bedragen voor deze route staan in `PRICING_NOTES.publishingFee`.
**Product category:** Website voor autobedrijven / occasionwebsite met voorraadkoppeling.
**Product type:** Abonnementsdienst (website als dienst), persoonlijk gebouwd en beheerd.
**Business model:** Eenmalige opstartprijs plus vast bedrag per maand, per pakket (Etalage, Verkoper, Dealer Pro). Je betaalt niet per auto. Stoppen betekent dat de site offline gaat; het platform en de broncode blijven van Occasly. Domein, content en leads blijven van de dealer en zijn mee te nemen. Kosten buiten Occasly (kanaaltarief Hexon via de voorraadleverancier, eigen portaalabonnementen) worden altijd genoemd.

## Target Audience

**Target companies:** Occasion- en autobedrijven in Nederland met ongeveer 5 tot 150 auto's op voorraad. Vaak een eigenaar-ondernemer, soms met een klein team. Werken met een voorraadsysteem of zetten auto's zelf op Marktplaats en AutoScout24.
**Decision-makers:** De eigenaar. Veelal 35 tot 60 jaar, praktisch ingesteld, geen techniekliefhebber.
**Primary use case:** Een eigen, professionele website waar de voorraad vanzelf op staat, zonder extra werk.
**Jobs to be done:**
- Online professioneel ogen, met eigen naam en uitstraling in plaats van alleen een advertentie op een portaal.
- Aanvragen (bellen, WhatsApp, proefrit, inruil) direct binnenkrijgen, zonder dat het extra werk kost.
- Geen gedoe met hosting, updates en een webbouwer die niet opneemt.

**Use cases:**
- Dealer met verouderde of trage site, voorraad in een kader (iframe) van een leverancier.
- Dealer zonder eigen site, alleen op Marktplaats/AutoScout24.
- Nieuw bedrijf dat nog een site nodig heeft.
- Dealer die wil doorgroeien: meerdere vestigingen, diensten, landingspagina's (Dealer Pro).

## Personas

- **Eigenaar (beslisser en gebruiker):** wil verkopen, niet met websites bezig zijn. Gevoelig voor eigen uitstraling, snelheid, transparante kosten en "niet nog een systeem erbij".
- **Verkoper/medewerker (gebruiker):** voert auto's in en beantwoordt aanvragen; wil dat het gewoon werkt.

## Problems & Pain Points

**Core problem:** De voorraad staat wel op de portalen, maar de eigen website is verouderd, traag, niet mobielvriendelijk, of toont de auto's alleen via een kader van een leverancier.
**Why alternatives fall short:**
- Alleen portalen: geen eigen merk, je betaalt per advertentie en de klant ziet ook de concurrent ernaast.
- Losse webbouwer: voorraadkoppeling is vaak een gedoe, onderhoud stopt, niemand neemt op.
- Doe-het-zelf-sitebouwers: voorraad dubbel invoeren of niet actueel.

**What it costs them:** Tijd (dubbel invoeren), aanvragen die niet binnenkomen, een slechtere eerste indruk dan de concurrent.
**Emotional tension:** Twijfel aan techniek, angst voor een "nieuw systeem", wantrouwen tegen webbouwers die na oplevering verdwijnen.

## Competitive Landscape

Nog niet onderzocht. Gebruik `competitor-profiling` voordat je concurrenten bij naam noemt. Noem nooit een concurrent in koude berichten.

**Direct:** andere aanbieders van dealerwebsites met voorraadkoppeling (uit te zoeken, inclusief websites die voorraadleveranciers zelf aanbieden).
**Secondary:** algemene webbureaus en WordPress-bouwers.
**Indirect:** alleen portalen (Marktplaats, AutoScout24) of geen website.

## Differentiation

**Key differentiators:**
- Werkwijze blijft hetzelfde: invoeren in je eigen voorraadsysteem, Occasly doet de rest.
- Eén vast bedrag per maand, niet per auto; kosten van derden staan er eerlijk bij.
- Eén persoonlijk aanspreekpunt dat je kunt bellen of appen (Robbert).
- Snel: de site laadt onder 1 seconde (claim op de homepage).
- In je eigen huisstijl; bij Dealer Pro maatwerk en huisstijlontwikkeling.

**How we do it differently:** Koppeling via Hexon met het systeem dat de dealer al heeft; geen nieuw systeem.
**Why that's better:** Geen dubbel werk, geen leercurve, voorraad altijd actueel.
**Why customers choose us:** Nog geen klanten (pre-launch). Gebruik geen klantverhalen tot ze er zijn.

## Objections

| Bezwaar | Antwoord (alleen met claims uit `outbound/claims.md`) |
|---|---|
| "Ik heb al een website." | Blijft je voorraad daar vanzelf actueel, met eigen pagina's per auto? Zo niet, dan laat de websitecheck zien wat er beter kan. |
| "Ik sta al op Marktplaats, dat is genoeg." | Portalen blijven; je eigen site komt erbij, met je eigen naam en zonder de concurrent ernaast. Portaalabonnementen sluit je zelf af. |
| "Wat kost het?" | Prijzen uit `packages.ts`, per pakket, plus de kosten van derden zoals ze daar staan. Nooit korting of afspraken: dat doet Robbert. |
| "Moet ik iets aan mijn systeem veranderen?" | Nee. Je vraagt de koppeling aan bij je leverancier, wij sturen de tekst mee en doen de rest. |
| "Is de site dan van mij?" | Het is een abonnement. Domein, content en leads blijven van jou en neem je mee. De site zelf draait op ons platform zolang het abonnement loopt. |

**Anti-persona:** Merkdealers van grote dealergroepen (centrale websites), pure export- of groothandelsbedrijven zonder consumentenverkoop, schadeherstel/demontage zonder occasionverkoop, bedrijven zonder auto's (scooters, caravans, aanhangwagens).

## Switching Dynamics

**Push:** verouderde of trage site, webbouwer onbereikbaar, voorraad dubbel invoeren.
**Pull:** eigen site die vanzelf klopt, vaste prijs, iemand die je kunt bellen.
**Habit:** "het werkt toch ook zo", alles via portalen.
**Anxiety:** gedoe met overstappen, extra kosten, vastzitten.

## Customer Language

**Words to use:** voorraad, occasions, je eigen site, automatisch, invoeren, voorraadsysteem, aanvragen, proefrit, inruil, bellen, appen.
**Words to avoid:** platform-jargon (API, feed, SaaS, tenant), "revolutionair", "uniek" of "maatwerk" voor Etalage en Verkoper, "binnenkort", "testfase", "wachtlijst".
**Glossary:** Hexon = koppelpartij die de voorraad van het voorraadsysteem doorzet; kanaaltarief = wat Hexon via de leverancier rekent.

## Brand Voice

- **Nuchter:** zeg wat het is. Niet: superlatievenregen. Voorbeeld: "Je blijft je auto's invoeren in VWE, zoals je gewend bent."
- **Direct:** korte, actieve zinnen, je-vorm. Niet: lange inleidingen.
- **Persoonlijk:** Robbert spreekt, eerste persoon. Niet: "ons team van experts".

**Tone by context:**
- Sales: concreet over hun eigen site, één vraag aan het eind.
- Support: kort en helpend.
- Social: praktisch, laat zien in plaats van vertellen.

**Vaste schrijfregels:** Nederlands, je-vorm, sentence case, geen em-streepjes (gebruik komma's of punten), knoppen en oproepen zeggen wat er gebeurt ("Plan een demo").
**Never use (and why):** "eigendom van de site" (het is een abonnement), "maatwerk" buiten Dealer Pro (wordt niet geleverd), bedragen die niet uit `packages.ts` komen.

## Proof Points

**Metrics:** Geen klantcijfers. Wel te noemen: drie demo-showrooms (demo.occasly.nl, demo2.occasly.nl, demo3.occasly.nl) met fictieve bedrijven.
**Customers:** Nog geen. Niet suggereren dat er klanten zijn.
**Testimonials:** Geen.
**Value themes:** geen dubbel werk, eigen uitstraling, vaste prijs, persoonlijk contact.

## Goals

**Business goal:** De eerste betalende dealers binnenhalen.
**Conversion action:** Een demo plannen (primaire CTA "Plan een demo"). Secundair: bellen of appen met Robbert (06 52 10 38 37).
**Current metrics:** Site nog pre-launch (noindex). Nog geen leadcijfers.

## Learnings

| Datum | Learning | Bron |
|---|---|---|
| | | |
