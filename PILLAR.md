# Pillar Configuration: Litfaß MUC (München)

> **Template Note:** This file isolates all city-specific parameters, local sources, and taste preferences.
> To adapt Litfaß to another city, update the values and lists below. The agent reads this file on every curation run.

---

## 1. City & Map Configuration

* **Pillar Name:** `Litfaß MUC`
* **City:** München (Munich), Germany
* **Language:** German (Deutsch) with casual, welcoming local phrasing
* **Map Center Coordinates:** `[48.1371, 11.5754]` (Munich Marienplatz / City Center)
* **Default Zoom Level:** `12`
* **Geographical Bounding Box (Lat/Lon):**
  * Minimum Latitude: `48.0500` (South: Pullach / Solln boundary)
  * Maximum Latitude: `48.2500` (North: Garching / Fröttmaning boundary)
  * Minimum Longitude: `11.3500` (West: Pasing / Aubing boundary)
  * Maximum Longitude: `11.7500` (East: Daglfing / Riem boundary)

*All event venues geocoded by the agent must fall inside this bounding box.*

---

## 2. Core Philosophy & Event Selection DNA

Litfaß is a **local radar for what makes Munich vibrant, open, and alive**—events that make you want to step outside and explore, even if just for an hour:
* **Spontaneous & Low-Barrier:** Events you can drop by without needing to buy tickets 6 months in advance. Free entry, donation, or spontaneous door admission.
* **City Life in Squares & Courtyards:** Bustling neighborhood squares, hidden courtyards, food trucks, and open-air public stages.
* **Civic & Cultural Vibrancy:** From neighborhood yard sales and museum vernissages to democracy manifestations and open-air university festivals.

---

## 3. Poster Hierarchy & Sizing Rules (Hero vs. Routine)

The agent must size posters in the Bento Grid based on **rarity, impact, and frequency**:

### A. Hero Posters (`format-hero`, Weight 9–10, Full Width)
**Strictly reserved for standout, landmark, or once-a-year/once-a-season events:**
* **Neighborhood Yard Sales (*Hofflohmärkte*):** e.g. Hofflohmarkt Maxvorstadt, Haidhausen, Glockenbach, Schwabing (each quarter only happens once a year!).
* **Traditional & Seasonal Landmark Bazaars:** *Auer Dult* (Maidult, Jakobidult, Kirchweihdult), *Zentraler Bauernmarkt* (z.B. Odeonsplatz/Ludwigstraße während der Wiesn), *Tollwood Festival* (Sommer/Winter), *Olympiapark Weihnachtsmarkt*.
* **Campus & Community Open-Air Festivals:** Free, open-access multi-stage festivals like *Garnix Open Air* (TUM Garching), *Tunix Open Air* (Königsplatz), *StuStaCulum*, *Theatron Pfingst/Sommerfestival* im Olympiapark.
* **Major Civic Manifestations:** Demonstrationen für Demokratie, Vielfalt & Menschenrechte auf Königsplatz, Odeonsplatz oder Theresienwiese.
* **Landmark Museum Openings & Special Nights:** Große Neueröffnungen/Ausstellungen an der *Pinakothek der Moderne*, *Haus der Kunst*, *Lenbachhaus*, *Lange Nacht der Münchner Museen*.

### B. Tall & Standard Posters (`format-tall` / `format-standard`, Weight 6–8)
**Distinctive monthly or bi-weekly community happenings:**
* Street food truck pop-ups and courtyard gatherings (*Alte Utting*, *Gans Woanders*, *Werksviertel-Mitte*).
* Natural wine releases, microbrewery courtyard tastings, specialty bakery pop-ups.
* Special bouldering, ninja warrior, or parkour community jams (*Boulderwelt*, *Heavens Gate*).
* Social group bike rides (gravel/road) or community run meetups.
* Free or low-cover intimate live sessions & courtyard acoustics (*Milla*, *Unter Deck*, *Import Export*).

### C. Compact Posters (`format-compact`, Weight 3–5)
**Frequent, recurring weekly events:**
* Weekly flea markets (*Daglfing*, *Olympiapark*).
* Weekly social runs or regular open training jams.
* Routine weekly courtyard DJ sessions or recurring open-mic evenings.

---

## 4. Taste Profile: The "YES" List
*Actively curate 12 to 24 standout happenings across these 4 categories:*

### A. Märkte, Vintage & Hofflohmärkte (`flea_market`)
* **Neighborhood Yard Sales (*Hofflohmärkte*):** High priority in central quarters: Maxvorstadt, Haidhausen, Glockenbach, Au, Schwabing, Sendling, Westend.
* **Landmark Bazaars & Traditional Markets:** *Auer Dult*, großer *Bauernmarkt* im Zentrum, *Midnightbazar*, Radlflohmärkte, Keramik- & Designmärkte.

### B. Food, Pop-Ups & Genuss (`food`)
* **Street Food Trucks & Courtyard Kitchens:** Pop-ups at *Alte Utting*, *Gans Woanders*, *Gans am Wasser*, *Bahnwärter Thiel*, *Sugar Mountain*.
* **Artisan & Craft Pop-Ups:** Natural wine & pét-nat tastings, specialty coffee & sourdough bakery events, local microbrewery open-airs.

### C. Kultur, Museen & Stadtleben (`concert`)
* **Museums & Visual Arts:** New exhibitions, vernissages, and special gallery nights at *Pinakothek der Moderne*, *Haus der Kunst*, *Museum Brandhorst*, *Lenbachhaus*, *Gasteig HP8*.
* **Open-Air & Low-Barrier Live Music:** Free-to-go festivals (*Garnix*, *Tunix*, *Theatron Olympiapark*, *Kulturstrand*), intimate club gigs with door entry (*Milla*, *Unter Deck*, *Import Export*).
* **Democracy & Civic Manifestations:** Pro-democracy rallies, solidarity manifestations, and civil society gatherings that bring the city together in public squares.

### D. Sport & Draußen (`sport`)
* **Individual Sports & Movement:** Bouldering & climbing community jams (*Boulderwelt Ost/West*, *Heavens Gate*), Ninja Warrior / Parkour / Calisthenics challenges.
* **Cycling & Running:** Road & gravel rides, social 5k–10k run clubs.
* **Casual Park Recreation:** Open-air Tischtennis tournaments, spikeball, outdoor yoga/mobility sessions in *Englischer Garten*, *Olympiapark*, *Isarauen*.

---

## 5. Taste Profile: The "NO" List
*Strictly filter out and ignore:*

* **Advance-Ticketed Mega Concerts:** Concerts requiring tickets bought months in advance, expensive arena tours, ticket lotteries.
* **Corporate & B2B Events:** Corporate networking mixers, trade fairs at *Messe München*, recruiting fairs, startup pitch competitions.
* **Commercial Pitch & Coaching Schemes:** Multi-level marketing (MLM), crypto/forex meetups, life-coaching seminars.
* **Overcrowded 'Instagram-Hype' Traps:** Overhyped pop-ups with artificial lines, steep admission, or purely commercial photo ops.
* **Routine Daily Opening Hours:** Venues merely open without a distinct special event.
* **Kids-Only / Esoteric Programs:** Pure toddler-only programs, astrology/crystal retreats.

---

## 6. High-Signal Local Sources to Monitor

1. `rausgegangen.de/muenchen`
2. `mitvergnuegen.com/muenchen`
3. `in-muenchen.de`
4. `hofflohmaerkte.de/muenchen`
5. `muenchen.de/veranstaltungen`
6. `pinakothek-der-moderne.de` & `hausderkunst.de`
7. Direct monthly programming for key community spaces:
   * Bahnwärter Thiel (`bahnwaerterthiel.de`)
   * Alte Utting (`alte-utting.de`)
   * Gans Woanders & Gans am Wasser (`ganswoanders.de`)
   * Import Export (`import-export.cc`)
   * Garnix / Tunix Open-Air (`garnix-openair.de`, `tunix.de`)
