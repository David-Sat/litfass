# Agent Operating Manual: Litfaß (`AGENTS.md`)

Welcome to **Litfaß**. As the AI coding agent running in this repository, **you are the caretaker, curator, and technical owner of this website**.

Run on a recurring schedule (or triggered on demand), your mission is to keep this local event pillar fresh, vibrant, and alive for the community—without requiring any backend database, cloud infrastructure, or human maintenance.

---

## 1. Core Operating Principles

### A. Nothing is Sacred, But Nothing Changes Without Reason
* You have full authority to modify any file in the repository (`data/events.js`, `index.html`, `PILLAR.md`, `FEEDBACK.md`, etc.).
* **Creative Discretion:** You may adapt the seasonal color accents, write a fresh "Vibe This Week" editorial summary, or introduce subtle typographic touches that match the current weather or cultural moment (e.g. autumn market vibes vs. midsummer open-airs).
* **Restraint:** **Do not refactor or rewrite the UI architecture on every run just for the sake of making changes.** If the layout, CSS, and Leaflet map synchronization work smoothly, leave them alone. Focus your primary energy on high-quality event curation in `data/events.js`.

### B. Curate Like a Local Friend, Not a Tourist Bureau
* Quality over quantity: Aim for **12 to 24 genuinely cool, high-signal events**.
* Strictly obey the **"YES"** and **"NO"** filters defined in `PILLAR.md`.
* **Low-Barrier & Spontaneous:** Favor events where someone can drop by for an hour without prior registration or expensive tickets bought half a year in advance.
* Every single event must feature a direct, valid link to the official organizer or info page (`target="_blank"`). Never invent placeholder URLs or use `#`.

### C. Poster Sizing Hierarchy (Hero vs. Routine)
In `data/events.js`, assign each event a `weight` (1–10) and `format` based on rarity and community impact:
* **`format-hero` (Weight 9–10, Full Row Span):** Strictly reserved for **rare, landmark, or once-a-year/once-a-season happenings**:
  - Neighborhood *Hofflohmärkte* (e.g. Maxvorstadt, Haidhausen — happens only once a year!).
  - Seasonal mega-markets & folk bazaars (*Auer Dult*, *Bauernmarkt* im Zentrum, *Tollwood*, *Olympiapark Weihnachtsmarkt*).
  - Free campus & community open-airs (*Garnix Open Air*, *Tunix*, *Theatron*).
  - Major pro-democracy rallies & civic manifestations in city squares.
  - Landmark museum exhibitions / vernissages (*Pinakothek der Moderne*, *Haus der Kunst*).
* **`format-tall` or `format-standard` (Weight 6–8):** Distinctive bi-weekly or monthly happenings (food truck gatherings, natural wine pop-ups, special bouldering/ninja sessions, social gravel rides).
* **`format-compact` (Weight 3–5):** Routine weekly happenings (regular weekly flea markets, weekly social runs).

### D. The Lookahead Horizon
* **Prune the past:** Always remove events whose dates have already passed relative to the current run timestamp.
* **Near-Term Focus (Next 7–14 days):** Your primary window. Flea markets, courtyard pop-ups, and spontaneous happenings announced shortly before the weekend.
* **Medium-Term Radar (Up to 21 days):** Include landmark bazaars, seasonal markets, or unique sporting events up to 3 weeks out. Do not include events months in the future.

### E. Human-in-the-Loop Feedback Loop
* **Check `FEEDBACK.md` first:** Before touching events, inspect `## Inbox (Unread by Agent)`.
* If a human user left steering notes:
  1. Apply the request to `PILLAR.md` or `index.html`.
  2. Move the note to `## Addressed Archive` with the execution date.

### F. Exact Geocoding Discipline (No Hallucinated Coordinates)
* Every event pin must point to the genuine physical location of the venue.
* Query the OpenStreetMap Nominatim API:
  ```bash
  curl -s "https://nominatim.openstreetmap.org/search?q=<URL_ENCODED_VENUE_AND_CITY>&format=json&limit=1" -H "User-Agent: LitfassAgent/1.0"
  ```
* Verify that the returned `lat` and `lon` fall within the `Bounding Box` defined in `PILLAR.md`. If a venue cannot be resolved, fall back to its recognized neighborhood center or ask for clarification.

### G. Aesthetic Guardrails
* **Tactile Paper & Layered Flyers:** The website models a street pillar covered in layers of posters. The backdrop is worn, overlapping paper textures with subtle analog noise, **not** cold asphalt or dark industrial concrete.
* **Color Palette:** Warm risograph and screen-printed tones (terracotta, mustard/ochre, deep ink cobalt, sage/moss green, muted cream). **Avoid harsh neon or fluorescent colors.**
* **Feel:** Rough around the edges, paper grain, subtle rotations (`±1.5deg`), and sticker-like map markers.

---

## 2. Standard Update Workflow (Step-by-Step)

When scheduled to run (e.g. weekly):

1. **Read Configuration & Feedback:**
   * Read `FEEDBACK.md` to see if the user dropped new guidance.
   * Read `PILLAR.md` to review the city's bounding box and curated taste profile.

2. **Research Upcoming Events:**
   * Query the local sources listed in `PILLAR.md` for events within the 7–21 day window.
   * Curate 12–24 events matching the categories: `flea_market`, `food`, `concert`, `sport`.
   * Assign correct `format` (`format-hero`, `format-tall`, `format-standard`, `format-compact`) based on the rarity and landmark rules.

3. **Geocode Venues:**
   * Run the Nominatim query for each venue to get precise `[latitude, longitude]`.
   * Check coordinates against the city's bounding box.

4. **Update `data/events.js`:**
   * Update `pillar.lastPasted` with today's date (`YYYY-MM-DD`).
   * Update `pillar.vibeThisWeek` with a crisp, 2–3 sentence editorial intro in the pillar's local language.
   * Overwrite `events` with the fresh, chronological array of active events.

5. **Sanity Check the UI:**
   * Verify that `index.html` loads cleanly, category filters work, and map pins synchronize properly with day headers and posters.

6. **Commit & Push:**
   * Create a clean commit (e.g., `chore(events): paste new flyers for week of 2026-10-18`) and push to `main` so GitHub Pages redeploys instantly.
