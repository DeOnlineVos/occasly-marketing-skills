# Outbound brief

Afspraken met Robbert (30 oktober 2026). Wijzigen alleen na zijn akkoord.

## Doelgroep en tiers

- **Land:** Nederland. Startregio: gemeente Heusden (Drunen, Vlijmen, Nieuwkuijk, Elshout, Haarsteeg, Heesbeen, Herpt, Heusden, Oudheusden). Daarna uitbreiden in ringen rond Den Bosch.
- **Bron:** RDW open data, bedrijven met erkenning Bedrijfsvoorraad (`opendata.rdw.nl`, datasets `5k74-3jha` en `nmwb-dqkz`).
- **Tier 1:** bedrijven met de hoogste score of een strategische waarde (groot, bekend in de regio). Elk bericht door Robbert goedgekeurd, ook later.
- **Tier 2:** goede score, verkoopt occasions aan consumenten, duidelijke aanleiding uit de websitecheck.
- **Tier 3:** past, maar zwakkere aanleiding.
- **Overslaan:** zie anti-persona in `../product-marketing.md`.

## Volume

- Start: 10 nieuwe contacten per werkdag, alleen na opwarmen van het verzenddomein.
- Later maximaal 20 nieuwe contacten per mailbox per werkdag.
- Maximaal 2 opvolgers, minstens 4 werkdagen ertussen.

## Akkoordregels

Autonomieniveau per actietype staat in het tabblad Instellingen van de Google Sheet "Occasly groeimotor". Startstand:

| Actie | Niveau |
|---|---|
| Bedrijven zoeken, verrijken, scoren | zelfstandig |
| Concepten en belbriefings maken | zelfstandig |
| Afmeldingen en afwezigheid verwerken | zelfstandig |
| Eerste mail, opvolgers | niveau 1 (Robbert keurt elk bericht) |
| Antwoorden op reacties | niveau 1 |
| Demo-aanvraag bevestigen en voorbereiden | niveau 1 |
| Prijzen, kortingen, voorwaarden, klachten, pers, partners | altijd Robbert |

Promotie: 50 voorstellen op rij van een type, minstens 45 zonder inhoudelijke aanpassing, geen klachten: dan niveau 2 voorstellen aan Robbert. Terugval naar niveau 1 bij een klacht, bounce boven 5 procent, een claim buiten `claims.md`, of twee afgekeurde steekproeven.

## Juridische keuze

Robbert heeft gekozen om koude e-mail toe te staan, ook als de rechtsvorm een eenmanszaak of vof is. Vaste regels per bericht, ook omdat ze de bezorgbaarheid beschermen:

- Echte afzender (Robbert Vos, Occasly) en telefoonnummer.
- Eén regel met de bron van het adres en een stopregel ("Antwoord met stop, dan mail ik je niet meer").
- Alleen algemene bedrijfsadressen (info@, verkoop@) van de eigen site van het bedrijf. Geen persoonlijke adressen raden.
- Rechtsvorm vastleggen in de Prospects-tab, zodat Robbert per groep kan kiezen.
- Op niveau 3 voor antwoorden: een regel dat het bericht met AI is opgesteld (AI-verordening art. 50).

## Kanalen en techniek

- Koude mail: verzenddomein `nl-occasly.nl` (Vimexx), één mailbox, gekoppeld aan lemlist via SMTP/IMAP met lemwarm aan. Open- en kliktracking uit. Nooit via Resend (daar lopen de leadmails van occasly.nl en straks de mail van dealers over).
- Aanvragen van occasly.nl staan in `site_leads` in de aparte Supabase-database van de site, niet in de platformdatabase.
- Bellen: Robbert, met een belbriefing van één scherm.
- LinkedIn: alleen handmatig door Robbert. Geen automatisering of scraping.

## Noodknop

Elke run leest eerst `Instellingen!B2` in de Google Sheet. Staat daar niet `aan`, dan stopt de run direct zonder iets te doen.
