## Bestanden in deze repository

```
.
├── README.md               # deze uitleg
├── content                 #
│   ├── 404.md              # voor ongeldige urls
│   ├── media               # map voor afbeeldingen etc.
│   └── publicaties         # map voor pagina's / posts op de website
├── data                    #
│   └── publicaties.yml     # lijst van publicaties, zie hieronder
├── hugo.toml               # globale configuratie
├── layouts                 #
│   ├── _default            # structuren van pagina's
│   └── shortcodes          #
└── static                  #
    ├── CNAME               # url van de website
    └── css                 #
        └── style.css       # vormgeving van de website
```

Site is gemaakt met [Hugo](https://gohugio.io). Elke keer als er een
bestand verandert hier op GitHub, wordt de website opnieuw _gebouwd_.

## Publicaties aan lijst toevoegen: `data/publicaties.yml`

Zie de [GitHub
documentatie](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files)
over hoe je een bestand aan kan passen in de browser.

In het bestand `data/publicaties.yml` staat een lijst van al je publicaties.
Elk nieuw onderdeel begint met een streep op het begin van de regel, gevolgd
door een spatie en dan de naam van het veld. Alle andere velden staan op de
regels eronder, die allemaal met twee spaties beginnen. Voorbeeld:

```yml
- hoofdtekst: "De 'titel' van het artikel"
  ondertekst: "De subtitel"
  date: 2024-08-21
  link: "/publicaties/lezingoranje/"
```

De link kan dus een url naar een andere website zijn, maar ook naar een artikel
op deze website in de `/content/publicaties/` map. Als het bestand
`/content/publicaties/lezingoranje.md` heet, is de url `/publicaties/lezingoranje/`. De
dubbele aanhalingstekens bij de `hoofdtekst`, `ondertekst` en `link` zijn
belangrijk! Anders kan je geen `:` gebruiken in de teksten.

## Tekstpagina aan website toevoegen: `content/publicaties/`

Zie de [GitHub
documentatie](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
over hoe je een bestand toevoegd aan de repository. Om een bestand te
verwijderen, Google "GitHub delete repository file".

Zoals hierboven al beschreven doe je dat in de map `/content/publicaties/`, als
bestandsnaam met enkel letters, cijfers en `-`. De bestandsextensie is `.md`.
Begin elk bestand met het volgende:

```md
---
title: "Titel hier"
date: 2024-01-01
---

Tekst hier
```

Om media toe te voegen aan de pagina's: voeg het bestand toe in de `/content/media`
map, en verwijs er op deze manier naar: `![voorbeeld
diagram](/media/diagram.jpg)`. Urls werken zonder het uitroepteken:
`[YouTube](https://youtube.com)`. Meer tips: Google op "markdown uitleg"
