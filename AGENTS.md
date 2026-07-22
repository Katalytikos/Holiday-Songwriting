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

At the end of each day (or whenever asked to sync):

1. Inspect changes under `Holiday Notes/` **and** `Diary/` since the last sync (git history, or compare against what is already quoted in `Songs/`).
2. Extract new observational fragments (images that stick, energy flows, encounters, thresholds, transitions, diary surprises / unresolved threads / refusing images).
3. Append them to the appropriate song file(s) under a dated heading:

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

4. Skip material already present in the song files. Skip pure process instructions unless they themselves become lyric material.
5. Commit with a message that names the date and which songs were updated.
