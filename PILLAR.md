# Pillar Configuration: Litfaß MUC (München)

> **Template Note:** This file isolates all city-specific parameters, local sources, and taste preferences.
> To adapt Litfaß to another city (e.g., Berlin, Vienna, Hamburg), simply update the values and lists below. The agent will read this file on every update run.

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

## 2. Taste Profile: The "YES" List
*Actively curate 12 to 24 standout happenings across these 4 primary categories:*

### A. Flohmärkte & Vintage (`flea_market`)
* **Neighborhood Yard Sales (*Hofflohmärkte*):** In Haidhausen, Glockenbach, Maxvorstadt, Neuhausen, Giesing, Sendling, Westend, Au.
* **Specialty Flea Markets:** *Krims & Krams* at Bahnwärter Thiel, *Midnightbazar*, *Flohmarkt Trabrennbahn Daglfing*, *Riesenflohmarkt Olympiapark*.
* **Bicycle, Record & Design Bazaars:** Radlflohmarkt, vinyl exchange meets, independent maker & ceramic pop-up markets.

### B. Street Food & Pop-Ups (`food`)
* **Culinary Pop-ups & Street Food:** Courtyard food markets, seasonal pop-up kitchens at *Alte Utting*, *Gans Woanders*, *Gans am Wasser*, *Werksviertel-Mitte (Container Collective)*.
* **Craft & Artisan Tastings:** Natural wine tastings, local microbrewery courtyard releases, street food weekends.

### C. Konzerte & Subkultur (`concert`)
* **Indie, Alternative & Electronic Live Gigs:** Intimate club concerts and off-beat showcases.
* **Favorite Cultural Spaces:** *Milla Club* (Glockenbach), *Unter Deck* (Altstadt), *Import Export* (Kreativquartier), *Bahnwärter Thiel* (Schlachthofviertel), *Muffatwerk / Ampere* (Haidhausen), *Feierwerk (Kranhalle & Hansa.39)* (Sendling), *Strom*, *Backstage*, *Gasteig HP8*.
* **Open-Air Cultural Stages:** *Theatron Olympiapark*, *Kulturstrand*, pop-up neighborhood stages.

### D. Sport & Draußen (`sport`)
* **Community Rides & Runs:** Social gravel rides, weekend road cycling meetups, social run clubs (e.g. along the Isar or through Englischer Garten).
* **Bouldering & Climbing Events:** Bouldering jams and community sessions (*Boulderwelt Ost/West*, *Heavens Gate*, *Einstein*).
* **Open-Air Park Sessions:** Outdoor yoga or fitness jams in *Olympiapark*, *Westpark*, or *Englischer Garten*.

---

## 3. Taste Profile: The "NO" List
*Strictly filter out and ignore any of the following:*

* **Corporate & B2B Events:** Corporate networking mixers, industry conferences at *Messe München*, corporate recruiting/career fairs, startup pitch competitions.
* **Commercial Pitch & Coaching Schemes:** Multi-level marketing (MLM), crypto/forex meetups, aggressive self-optimization seminars, life-coaching workshops.
* **Standard Tourist Traps:** Hop-on-hop-off bus promotions, daily Hofbräuhaus tourist shows, generic souvenir fairs.
* **Routine Daily Opening Hours:** Merely open venues without an actual special event (e.g., "Viktualienmarkt is open on Tuesday" is NOT an event).
* **Kids-Only / Esoteric Programs:** Pure toddler/kindergarten-only plays, astrology/crystal retreats, dog obedience shows.

---

## 4. High-Signal Local Sources to Monitor

When researching upcoming dates in Munich, check:
1. `rausgegangen.de/muenchen`
2. `mitvergnuegen.com/muenchen`
3. `in-muenchen.de`
4. `hofflohmaerkte.de/muenchen`
5. `muenchen.de/veranstaltungen`
6. Direct monthly programming for key cultural spaces:
   * Bahnwärter Thiel (`bahnwaerterthiel.de`)
   * Alte Utting (`alte-utting.de`)
   * Gans Woanders & Gans am Wasser (`ganswoanders.de`)
   * Import Export (`import-export.cc`)
   * Milla Club (`milla-club.de`)
   * Muffatwerk (`muffatwerk.de`)
   * Feierwerk (`feierwerk.de`)
