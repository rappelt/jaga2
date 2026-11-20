---
title: JAGA Website V2
aliases: [JAGA Trendy Website, jaga-trendy V2]
tags: [projekt/jaga, website, ci, astro, vercel]
status: live
created: 2026-11-20
updated: 2026-11-20
live: https://jaga-trendy.vercel.app/
repo: https://github.com/rappelt/jaga-trendy
---

# JAGA Website V2

Neue Website für **JAGA Sp. z o.o.** (Marke *JAGA Trendy*), Gdańsk: B2B-Spezifikationspartner für Contract-Möbel zwischen Architekten und 13 europäischen Herstellern.

- **Live:** https://jaga-trendy.vercel.app/ (PL `/pl/`, EN `/en/`, DE `/de/`)
- **Code:** [rappelt/jaga-trendy](https://github.com/rappelt/jaga-trendy), Branch `master`, Deploy automatisch über Vercel
- **Analyse, CI-Brief, Mockups:** [rappelt/jaga2](https://github.com/rappelt/jaga2) (Branch `claude/pensive-mccarthy-co68pv`)
- **Übersicht (Artifact):** https://claude.ai/artifact/CYFHkbtZ3MBtv7mctBBSwB (DE) · https://claude.ai/artifact/BBpGNTxKgyDMuwX8nnP4iK (EN)

## Firmendaten (geprüft)

| Feld | Wert | Quelle |
|---|---|---|
| Firma | JAGA Sp. z o.o. | Weiße Liste (Finanzministerium PL), EU VIES |
| Marke | JAGA Trendy | |
| Sitz | ul. Bolesława Chrobrego 79F, 80-414 Gdańsk | Weiße Liste, VIES |
| KRS | 0000150770 | Weiße Liste |
| NIP | 593-010-23-29 | Weiße Liste |
| REGON | 190247090 | Weiße Liste |
| USt-IdNr. (EU) | PL5930102329, gültig | VIES, 20.11.2026 |
| Umsatzsteuer | aktiv (czynny) | Weiße Liste |
| Telefon | +48 58 554 16 16 | Firmenverzeichnisse, **bitte bestätigen** |
| E-Mail | gdansk@jagatrendy.pl | Firmenverzeichnisse |

Noch aus dem KRS ergänzen: Vorstand (Zarząd), Stammkapital (Pflicht nach Art. 206 KSH), Registergericht. Die KRS-API war am 20.11. abends in Wartung.

## Wettbewerb (Kurzfassung)

14 Seiten geprüft, 11 auswertbar: .mdd, Nowy Styl, 9design (PL), Alax (CZ), smow, architare (DE), De Projectinrichter (NL), Contract Furniture Store (UK), Living Edge, Space Furniture, Stylecraft (AU).

- **Stark im Markt:** „Für Architekten“ im Hauptmenü, Einstieg nach Branche, Referenzen mit Ort/Architekt/Umfang.
- **Schwach im Markt:** Rabatte im Hero, Warenkorb statt Anfrageliste, B2B versteckt.
- **Lücke für JAGA:** CAD/BIM + Musterservice prominent, Sprache der Architekten (Positionsnummern, Möbelliste), eine Projektliste über alle Marken.

Details: `docs/wettbewerbsanalyse.md` im Repo jaga2.

## CI

- **Positionierung:** Der Spezifikationspartner zwischen Architekten und Europas Contract-Herstellern.
- **Claim:** Od planu do miejsca. / Vom Plan zum Platz. / From plan to place.
- **Farben (nach neuem Logo):** Ink `#16232B` · Signal-Orange `#FF6A30` (Text auf Hell: `#A8401A`) · Slate `#54616A` · Fog `#ECEEEC` · Pier `#C9CFCB`
- **Schrift:** Archivo (variabel, Breite 62–125), selbst gehostet über `@fontsource-variable/archivo` (DSGVO, kein Google-Request)
- **Signatur:** Spec-Tag (CH-01, ST-02 …) als Positionsmarke
- **Logo:** `src/assets/jaga-logo-v2.png`, Variante für dunkel `jaga-logo-v2-on-dark.png`
- **Favicon:** aus der Bildmarke nachgezeichnet, `public/favicon.svg` + `.ico` + Apple/Android-Icons

## Startseite (Entwurf A „Spec“)

1. Hero mit Spec-Tags im Restaurantfoto (Position → Projektliste)
2. Einstieg nach Branche
3. Mitlaufende FF&E-Möbelliste mit „Zur Liste“
4. 13 Hersteller mit „Zur Liste“
5. Architekten-Servicedesk (CAD/BIM, Muster, Ausschreibung, Vergleich)
6. Fünf Schritte als horizontale Zeitleiste (aus Entwurf B)
7. Projekte als Sticky-Streifen
8. Kontakt: Formular (→ `/api/leads` → Supabase) + Sprachassistent (Live-Assistent aus [[Telefon-Assistent]])

**Projektliste:** pro Browser in `localStorage`, Zähler im Header, wird an die Anfrage angehängt (Startseite und Kontaktseite).

## Hersteller und Logos

Echte Logos: LAS, Wilkhahn, Profim, Bejot, Alias, Softline, Infiniti, Pedrali, Thonet (von den Herstellerseiten), Magis (Wikimedia Commons, CC BY-SA 4.0).

Noch ohne Logo (Name als Schrift): **Plust, TON, Paged**. Offizielle Dateien über Pressebereich oder Ansprechpartner anfordern. TON hat ein neues Logo (Kreis statt Stuhl).

Die alten Logos waren KI-generiert mit verstümmeltem Text und wurden entfernt. Infiniti korrigiert: Name (vorher „Infinity“) und Link (vorher australischer Händler, jetzt infinitidesign.it).

## Pull Requests (jaga-trendy)

- [#3](https://github.com/rappelt/jaga-trendy/pull/3) Neues CI + Startseite (Entwurf A)
- [#4](https://github.com/rappelt/jaga-trendy/pull/4) Projektliste überall, Silbentrennung, Sprachwahl im Handy-Menü
- [#5](https://github.com/rappelt/jaga-trendy/pull/5) Echte Herstellerlogos
- [#6](https://github.com/rappelt/jaga-trendy/pull/6) Favicon, Logos klickbar (neuer Tab)
- [#7](https://github.com/rappelt/jaga-trendy/pull/7) Impressum mit geprüften Firmendaten, Firmenname überall korrigiert

## Technische Hinweise

- Bilder auf der Startseite sind statische Dateien (`<img src={bild.src}>`), keine Laufzeit-Optimierung: `astro:assets <Image>` braucht `sharp` in der Vercel-Funktion und lieferte dort keine Bilder.
- Silbentrennung über `hyphens: auto` nach Seitensprache (`html lang`). Geprüft: 3 Sprachen × 5 Seiten × 4 Breiten ohne Überlauf.
- Sprachassistent funktioniert nur auf freigegebenen Domains: Zentrale prüft `ANRUF_ALLOWED_ORIGINS` (Vercel-Projekt telefon-assistent). Vorschau-URLs sind dort nicht freigegeben.
- Cloud-Umgebung „JAGA Website V2“: freigegebene Hosts u. a. für Herstellerseiten, KRS-API, Weiße Liste, VIES.

## Offene Punkte

- [ ] Vorstand, Stammkapital, Registergericht aus KRS ins Impressum
- [ ] Telefonnummer +48 58 554 16 16 bestätigen
- [ ] Logos Plust, TON, Paged
- [ ] Eigene Projektfotos statt Unsplash-Platzhalter
- [ ] Polnische und deutsche Texte von Muttersprachlern gegenlesen
- [ ] Herstellerlogos: Nutzung mit den Marken bestätigen
