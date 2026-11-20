# JAGA Website V2: Analyse und Wettbewerb

Stand: 20.11.2026. Alle Seiten wurden live aufgerufen und per Playwright erfasst (Screenshots in `competitor-screens/`).

## 1. Ist-Analyse: jaga-trendy.vercel.app

**Geschäft:** JAGA Trendy Sp. z o.o., Gdańsk. B2B-Spezifikations- und Beschaffungspartner für Contract-Möbel (Hotel, Gastronomie, Büro, Retail, öffentliche Räume). Zielgruppen: Architekten, Planer, Interior Designer, Betreiber. Märkte: PL (primär), DE, international. Sprachen: PL, EN, DE.

**Hersteller (13):** Pedrali, Magis, Plust, Thonet, Infiniti (Café/Restaurant) · Paged, TON (Holzstühle) · Alias, Softline (Sofas) · Wilkhahn, Profim, Bejot (Bürostühle) · LAS (Bürosysteme).

**Referenzen (Seed-Daten):** Hard Rock Cafe Warschau (200+ Stühle, Barhocker, Polster, PAGED, Fameg) · Premium Office Berlin (120+ Arbeitsplätze) · Boutique-Hotel Krakau (80+ Möbel, Fameg).

**Stärken:** klare B2B-Abgrenzung, eigene Architekten-Ansprache, dreisprachig, Astro-Basis, starke Herstellerliste.

**Schwächen:**
- **Hersteller-Logos sind KI-generierte Fälschungen** mit verstümmeltem Text (Infiniti „FUNRN HLURE“, Pedrali „INSIIUANT FURRANY“, Thonet und TON als Stuhlfotos, Plust und Wilkhahn weiß auf weiß). Markenrechtliches Risiko. Offizielle Logos bei den Herstellern anfordern. Die Mockups setzen die Namen deshalb als Schrift.
- Impressum mit Platzhaltern (Warszawa, Nullnummern, „Jan Kowalski"), widerspricht der Kontaktseite (Gdańsk). **Rechtlich zuerst beheben.**
- Unbelegte Aussagen („verified partners", „24 h", „100 % B2B"), keine Telefonnummer.
- Zwei generische Stockfotos, je doppelt verwendet; keine Projektfotos.
- Vier konkurrierende Akzentsysteme (Amber, Blau-400, Rot/Orange-Buttons, oranges Voice-Panel), keine Webfont.
- Deutsche Texte fest in EN/PL-Startseite, Projektnamen uneinheitlich zwischen Startseite und Datenbank.
- Gleiches Muster (Eyebrow, H2, grauer Absatz) in jedem Abschnitt, gleiche zwei CTAs etwa siebenmal.

## 2. Wettbewerber

14 Seiten geprüft, 11 auswertbar. lino.cz, mesmetric.com und utilitydesign.co.uk blockierten den automatischen Zugriff (Cloudflare).

| Anbieter | Land | Modell | Stärken | Schwächen | Idee für JAGA |
|---|---|---|---|---|---|
| .mdd (mdd.eu) | PL | Hersteller Office/Contract | Hero „Spaces made better" mit einem Satz, einem CTA, großem Raumfoto; „For Architects" und „B2B" im Hauptmenü; Projektgalerie mit Architekt und Fotograf | Nur eigene Marke; Preisanzeige verwässert B2B; Projektlisten textlastig | Projektgalerie mit Credits |
| Nowy Styl (nowystyl.com) | PL | Großhersteller, 70+ Länder | Navigation nach Räumen (Hotel, Restaurant, Office, Healthcare); Knowledge-Hub; Partner Zone für Architekten | Hero nur ORGATEC-Kampagne; Burger-Menü auf Desktop; Office-lastig | Einstieg „nach Raum" |
| 9design (9design.pl) | PL | Händler, Showroom Warschau 350 m² | Architekten-Servicebüro, 3D-Modelle, empfohlene Architekten, Investoren-Track, 3D-Rundgang | Retail-Optik, Rabatt-Pop-up, Darstellungsfehler | Architekten-Servicebüro |
| Alax (alax.cz) | CZ | Händler mit Contract (führt Pedrali, Bejot) | Segmente; PROFIZONE-Login; Telefon im Header | Dichtes Mega-Menü; 12,8 px Schrift; Sprachmix | Profi-Bereich mit Downloads |
| smow (smow.de) | DE | Design-Händler, ca. 17 Stores, „smow works" | Lieferzeit auf jeder Karte; Beratung buchbar; Trusted Shops 4,81 | Konsumenten-lastig; B2B im Footer | Lieferzeit/Musterverfügbarkeit zeigen |
| architare (architare.de) | DE | Premiumhändler mit Planung | Service-IA (Office-Planung, New Work Lab); Einzeiler je Marke | Visuell nicht bewertbar | Ein-Satz-Statement pro Hersteller |
| De Projectinrichter | NL | Markenunabhängig, 250+ Marken | Angebotsliste statt Warenkorb; Phasenmodell; Zertifikate, Kreislauf | Template-Optik; Script-Font-Bruch | Herstellerübergreifende Projektliste |
| Contract Furniture Store | UK | Spezialist europäische Contract-Möbel | „Start your project by sector"; „Send us your specification"; Kundenlogos | Generisches Shopify; SEO-Fülltext | Branchen-Einstieg unter dem Hero |
| Living Edge | AU | Händler (Herman Miller u. a.) | Sofortige Weiche Home/Professional | Inhalt hinter Gate; Kontrast | Dauerhafter „Für Architekten"-Einstieg |
| Space Furniture | AU | Importeur, Showrooms | Services nach Trade/Commercial/Architectural; Journal | Hero mit 50 % Sale | Klare Service-Taxonomie |
| Stylecraft | AU | Importeur/Contract seit 1953 | Sektor-Kacheln; Projekte mit Kundennamen; Showroom je Stadt | Outlet-Sale im Hero; kein Haupt-CTA | Referenzen mit Ort, Sektor, Umfang |

## 3. Synthese

**Was die Besten richtig machen:** Profis im Hauptmenü abholen · Einstieg nach Branche/Raum · Referenzen mit Ort, Architekt, Umfang · ruhige fotogeführte Gestaltung mit einem Akzent.

**Wo fast alle schwach sind:** Rabatte im Hero · Warenkorb statt Anfrageliste · B2B versteckt · austauschbare Optik (weiß/schwarz/gelb).

**Lücke für JAGA:** CAD/BIM und Musterservice prominent · Sprache der Architekten (Positionsnummern, Möbelliste, Ausschreibung) · herstellerübergreifende Projektliste mit einer Anfrage.

## 4. Neues CI (Kurzfassung, Details in `ci/BRIEF.md`)

- **Positionierung:** Der Spezifikationspartner zwischen Architekten und Europas Contract-Herstellern.
- **Claim:** Od planu do miejsca. / Vom Plan zum Platz. / From plan to place.
- **Farben (Gdańsk):** Baltic Ink #16232B · Bursztyn #E2891C · Bursztyn tief #A65E0B · Cegła #8E3B2B · Mgła #ECEEEC · Molo #C9CFCB
- **Schrift:** Archivo (variabel). Expanded 800 für Headlines, Normal für Text, Condensed 600 für Codes.
- **Signatur:** Spec-Tag (CH-01, ST-02 …) als Hotspot, Listenpunkt, Umfangsangabe.
- **Logo:** Bernstein-Raumecke und Stuhl-Quadrat plus Wortmarke JAGA (`ci/logo.svg`).
- **Bewegung:** Scroll-Technik der Interior-Seite (rAF-Loop, CSS-Variablen, Parallaxe, Linienzeichnung, Fortschrittslinie, Sticky-Streifen), mit Reduced-Motion-Fallback.
