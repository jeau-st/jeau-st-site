# jeau-st-site

Website van Jeau.st (jeau.st), de eenmanszaak van Joost Beers. Vervangt de oude WordPress-site op Cloud86.

## Kern

- Doel: een bezoeker die twijfelt laten mailen voor een gesprek (joost@jeau.st). Geen formulier, geen nieuwsbrief, geen blog.
- Ontwerp en copy: volg `REDESIGN_BRIEF.md`. Dat is de opdracht; dit bestand is alleen de context.
- Taal: Nederlands. Geen em dash. Nuchter, geen consultancytaal.

## Stack

- Eén statische `index.html`, vanilla JS alleen waar nodig, geen framework.
- Tailwind CSS v4 via de CLI: `src/input.css` naar `css/style.css`. Nooit de Play CDN.
- Assets in `img/` (logo, favicons, toollogo's).

## Commando's

```
npm install
npm run dev     # Tailwind watch
npm run build   # css/style.css geminificeerd
```

`css/style.css` wordt ingecheckt, want hosting heeft geen build-stap.

## Hosting

- Nu: GitHub Pages met `CNAME` (jeau.st).
- Gepland: Cloudflare (Workers static assets of Pages), net als de andere sites.
- Open risico: de mail van joost@jeau.st loopt via Microsoft 365. Controleer MX-, SPF- en DKIM-records voordat DNS of Cloud86 wordt aangepast.

## Regels

- Geen verzonnen testimonials, klantcases, cijfers, certificeringen of partnerstatus.
- Kleuren en fonts alleen via tokens in `@theme` in `src/input.css`.
- Geen secrets in de repo.
