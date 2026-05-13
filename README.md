# themovingbreath — Website

Statische GitHub Pages Website für Lu (Yoga & Breathwork).
Instagram: [@themovingbreath](https://www.instagram.com/themovingbreath/)

## Verzeichnisstruktur

```
/
├── index.html              ← Landing Page (DE + EN, mit Sprach-Toggle)
├── impressum.html
├── datenschutz.html
├── images/
│   └── logo.png            ← Logo (Lu)
└── fonts/
    ├── cormorant-garamond-300.woff2
    ├── cormorant-garamond-400.woff2
    ├── cormorant-garamond-500.woff2
    ├── cormorant-garamond-600.woff2
    ├── inter-300.woff2
    ├── inter-400.woff2
    └── inter-500.woff2
```

## Schriftarten (lokal)

Alle HTML-Seiten laden Schriften lokal aus `/fonts/` via `@font-face`:

- **Cormorant Garamond** — Gewichte 300, 400, 500, 600 (Headlines, Zitate)
- **Inter** — Gewichte 300, 400, 500 (Body, Navigation, Buttons)

Kursive Varianten werden vom Browser synthetisiert (entspricht der gleichen Strategie wie beim Zapf-Projekt).

## Sprach-Toggle (DE / EN)

`index.html` enthält Deutsch und Englisch parallel:

- Jedes mehrsprachige Element hat `data-de="…" data-en="…"`.
- Header-Button (`EN` / `DE`) wechselt die Sprache. Auswahl wird in `localStorage` (`tmb-lang`) gespeichert.
- Default beim ersten Besuch: Deutsch.
- `impressum.html` und `datenschutz.html` bleiben rechtsbedingt Deutsch.

## Inline-SVG-Ferne

Ein wiederverwendbares `<symbol id="fern">` ganz oben im `<body>`, referenziert via `<use href="#fern"/>`. Dezent platziert: Hero-Hintergrund, in jeder Angebot-Karte, neben dem Zitat, im Footer.

## Platzhalter ersetzen

In `index.html`, `impressum.html` und `datenschutz.html` sind offene Stellen mit `[PLATZHALTER: …]` markiert (visuell hervorgehoben). Noch ausstehend von Lu:

- Vollständiger Name (Inhaberin) — Impressum & Datenschutz
- Postanschrift (Straße, PLZ, Stadt) — Impressum & Datenschutz
- E-Mail-Adresse — Impressum, Datenschutz, Stundenplan-Sektion
- Telefonnummer (optional)
- USt-IdNr. — oder Block entfernen (Kleinunternehmerregelung § 19 UStG)
- Tätigkeitsbeschreibung & ggf. Berufshaftpflicht
- Zuständige Landesdatenschutzbehörde (richtet sich nach dem Bundesland des Wohnsitzes)
- Ort (im Hero und Footer)
- Studio-Adresse & Stadt (Stundenplan-Sektion)
- Aktuelle Kurszeiten
- Preise (Drop-In, 10er-Karte)
- Datum „Stand: …"

## Custom Domain einrichten (wenn bereit)

Lu setzt im Registrar folgende DNS-A-Records auf GitHub Pages:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Dann unter **Settings → Pages → Custom domain** die Domain eintragen und „Enforce HTTPS" aktivieren.

## Pre-Launch-Checkliste

- [ ] Alle `[PLATZHALTER: …]` ersetzt
- [x] Schriftdateien in `/fonts/` liegen
- [x] `index.html` auf lokale Fonts umgestellt
- [x] Footer-Links zu Impressum und Datenschutz funktionieren
- [x] DE/EN-Sprach-Toggle funktioniert und wird persistiert
- [ ] Auf Mobilgeräten getestet
- [ ] Custom Domain eingerichtet und HTTPS aktiv
