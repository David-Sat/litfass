# 🗞️ Litfaß

> **Zero-backend, autonomous local event discovery modeled after a traditional German *Litfaßsäule*.**  
> Maintained, geocoded, and updated on schedule by an AI coding agent (**Google Antigravity** or **Claude Code**) and hosted for free on **GitHub Pages**.

---

## ✦ What is Litfaß?

A traditional *Litfaßsäule* is the iconic street cylinder found throughout German, Austrian, and European cities—weathered and thick with layers of pasted paper flyers announcing neighborhood flea markets, intimate club concerts, street food pop-ups, and community gatherings.

**Litfaß** brings this physical-digital metaphor to the web:
* **No Database or Cloud Servers:** 100% static, zero-build HTML/CSS/ES6+ JavaScript.
* **Agent-Maintained:** An AI coding agent owns the repository. Run on a recurring schedule, it researches upcoming events based on a human-curated taste profile, geocodes exact venues using OpenStreetMap Nominatim, pastes new flyers onto the site, peels off expired events, and commits the updates.
* **Tactile Paper Aesthetic:** Layered paper textures, screenprint and risograph color accents, tape strips, and subtle rotations—never sterile corporate dashboards or cold asphalt.
* **Bidirectional Map ↔ Calendar Sync:** A split-screen layout pairing chronological day feeds with an interactive Leaflet city map. Hovering date headers highlights all pins for that day; clicking map markers smoothly scrolls to that poster.

---

## 🏛️ Two-Tier Repository Architecture

This repository is built as an open **GitHub Template Repository** that anyone can fork or clone to create an autonomous pillar for any city:

```text
/
├── index.html       # Standalone interactive UI (Wheatpaste cards + Leaflet map sync)
├── data/
│   └── events.js    # Clean data store (updated autonomously by the agent)
├── AGENTS.md        # The agent's brain: operating principles, lookahead rules & geocoding
├── PILLAR.md        # City configuration: coordinates, bounding box & YES/NO taste filters
├── FEEDBACK.md      # Human steering inbox & addressed archive
└── README.md        # Documentation & setup guide
```

1. **`AGENTS.md` (The Universal Engine):** Operating instructions for AI agents (Antigravity, Claude Code). Details geocoding rules, lookahead horizons (7–21 days), and maintenance discipline (*"Nothing is sacred, but nothing changes without reason"*).
2. **`PILLAR.md` (The City & Taste Profile):** Isolates all city-specific parameters (City name, center coordinates, bounding box, curated YES/NO event filters, and local high-signal sources).
3. **`FEEDBACK.md` (Human-in-the-Loop Steering):** A low-friction inbox where you can drop quick steering notes anytime (e.g., *"Too many techno clubs, add more daytime flea markets"*). On its next run, the agent reads the note, permanently folds the preference into `PILLAR.md`, and moves it to the archive.
4. **`data/events.js` (Separated Data Store):** Keeps event data decoupled from the UI markup, ensuring that scheduled agent runs update events safely without touching or risking regressions in `index.html`.

---

## 🚀 Spin Up Your Own City Pillar (5 Minutes)

### 1. Create Your Repository
1. Click **"Use this template"** > **"Create a new repository"** at the top of this repo (e.g., name it `litfass-berlin` or `litfass-vienna`).
2. Clone your new repo locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/litfass-YOUR_CITY.git
   cd litfass-YOUR_CITY
   ```

### 2. Enable GitHub Pages
1. Go to your repository settings on GitHub: **Settings** > **Pages**.
2. Under **Build and deployment** > **Source**, select **Deploy from a branch**.
3. Choose branch: `main` and folder: `/ (root)`. Click **Save**.
4. Your site will be live at `https://YOUR_USERNAME.github.io/litfass-YOUR_CITY/` in ~60 seconds.

### 3. Customize `PILLAR.md` for Your City
Open `PILLAR.md` and edit:
* **City Name & Pillar Title:** (e.g., `Litfaß BER` / Berlin)
* **Map Center & Bounding Box:** Get target coordinates for your city center.
* **The "YES" and "NO" Lists:** Customize local genres, favorite neighborhood flea markets, indie venues, and community groups.
* **Local Sources:** List 4–6 high-signal local blogs, magazine event calendars, or cultural hubs.

### 4. Schedule Weekly Updates with Your AI Agent

#### Via Google Antigravity:
Run the `/schedule` command or prompt Antigravity:
```text
Run the Litfaß weekly curation workflow defined in AGENTS.md for my city in PILLAR.md.
Check FEEDBACK.md, research verified upcoming events, geocode venues, update data/events.js, and commit.
```

#### Via Claude Code (`claude`):
You can run Claude Code on a weekly cron job or local scheduled task:
```bash
claude "Execute the Litfaß weekly curation cycle in AGENTS.md. Check FEEDBACK.md, update data/events.js, and push to main."
```

---

## 🛠️ Local Development & Testing

No Node.js, npm, or build step is required. Simply open `index.html` in any modern web browser:

```bash
# Option 1: Direct file preview
open index.html

# Option 2: Simple Python local server
python3 -m http.server 8000
# Open http://localhost:8000
```

---

## 📜 License
MIT License. Open source and free for independent cultural organizers, neighborhood communities, and local enthusiasts.
