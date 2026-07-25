# Agent instructions — Holiday Songwriting

## Song routing from Holiday Notes and Diary

Each song in `Songs/` is a day-phase vessel. When observations appear in `Holiday Notes/` or `Diary/` (daily notes), append them to the matching song file(s). Keep the song’s opening time-slot line intact. Prefer short observational fragments over copying long AI essays wholesale.

| Song file | Day phase | Route notes about… |
|---|---|---|
| `Songs/(Fighting entropy).md` | Early morning — metabolism / emergence | Awakening, metabolism, entropy, open systems, regeneration, morning rituals, food emerging from process, age/injury as entropy |
| `Songs/The life of water.md` | Morning → midday — encounters | Pool, water, thresholds (edges, doors, shutters), encounters / “what becomes possible when X meets Y”, submerging, reflections, light in water, shared swimming |
| `Songs/Causeways of the sun.md` | Midday → evening — energy | Heat, sun, energy gathering/dissipating, shade, fans/air-con, afternoon heat, insects in heat, sun→pool energy chains, book/title seeds about sun paths |
| `Songs/The blue hour.md` | Evening → night — liminality | Blue hour, dusk/night transitions, evening company, cooling, liminality, silhouettes, unresolved endings |

An observation may belong to more than one song; append it wherever it fits. Do not invent lyrics unless asked — collect and route field notes.

## End-of-day sync

**Schedule:** every evening at **22:00** Europe/Paris (CEST/CET — matching phone commit timezone), and whenever asked to “Sync now”.

When the scheduled automation or a manual sync runs:

1. Pull / inspect the latest `main`.
2. Inspect changes under `Holiday Notes/` **and** `Diary/` since the last sync (git history, or compare against what is already quoted in `Songs/`).
3. Extract new observational fragments (images that stick, energy flows, encounters, thresholds, transitions, diary surprises / unresolved threads / refusing images).
4. Append them to the appropriate song file(s) under a dated heading:

   ```markdown
   ## From Holiday Notes — YYYY-MM-DD

   ### <source note title>
   - observation…
   ```

   ```markdown
   ## From Diary — YYYY-MM-DD

   - observation…
   ```

   Use the diary entry’s own date for `From Diary` headings. Use the sync date for `From Holiday Notes` headings (append to the same day’s section if one already exists).

5. Skip material already present in the song files. Skip pure process instructions unless they themselves become lyric material.
6. If there is nothing new, make no file changes (open no PR).
7. Otherwise commit, push a `cursor/…-2e32` branch, and open/update a PR into `main` with a message that names the date and which songs were updated.
8. **Merge the PR into `main` before finishing** (mark ready if draft, then merge and delete the branch). Do this every sync — do not leave the PR open.

### Cursor Automation setup (for the owner)

Create at [cursor.com/automations](https://cursor.com/automations):

- **Trigger:** Scheduled — daily at 22:00 (Europe/Paris), or cron `0 20 * * *` UTC while on CEST / `0 21 * * *` UTC on CET
- **Repository:** `Katalytikos/Holiday-Songwriting`, branch `main`
- **Prompt:**

  ```
  Follow AGENTS.md. Sync now: inspect Holiday Notes/ and Diary/ for changes since the last sync, append new observations to the matching Songs/ files, commit, push, open a PR into main, and merge that PR. If nothing new, do not open a PR.
  ```
