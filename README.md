# DynaMik Padel Academy

Static website for DynaMik Padel Academy — all-inclusive padel camps on the Costa Blanca.

- `index.html` — the full site (HTML, CSS and JS in one file), in FR / NL / EN / DE / ES
- `media/` — hero video, photos and logo

No build step. Deployed on Vercel as a static site.

## To do before launch

- Booking form does not send yet: wire the submit handler in `index.html` (search for `TODO launch`) to an endpoint.
- Packages, sample itinerary and FAQ answers are placeholder copy; replace with the real offer and prices.
- Add contact details.
## Beheerpagina (`/beheer.html`)

Klantbeheer voor teksten en foto's (Solyn Global), zonder server of database. Zelfde werkwijze als bij Nuance.

- Openen: `/beheer.html`, toegangscode `dynamik` (houdt alleen toevallige bezoekers weg; `noindex`).
- Klant kiest een pagina, tikt op een tekst en typt; foto's vervangen via het tabblad Foto's. Met de knop "Klikken" werkt de site weer gewoon (taal wisselen, menu openen, doorklikken). Werkt als app op telefoon (manifest + service worker, enkel voor `/beheer`).
- Wijzigingen blijven op het toestel van de klant. Met "Versturen" komt een bestand `dynamik-wijzigingen.txt` binnen via WhatsApp/mail.
- Online zetten: nakijken en de inhoud als `site-content.js` in de repo zetten. `site-edit.js` past die toe op elke pagina (ook na React-renders). Leeg bestand = site zoals gebouwd.
- Teksten zijn gekoppeld aan hun oorspronkelijke tekst, foto's aan hun oorspronkelijke bestand. Wordt die bron later in de code veranderd, dan vervalt de oude aanpassing.
- Achtergrondafbeeldingen in CSS en video's zijn niet via het beheer aan te passen.
