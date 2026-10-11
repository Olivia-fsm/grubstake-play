# Audio drop-in

Everything the game plays is synthesised at runtime (`src/audio/engine.ts`). To use licensed or generated audio instead:

- Music: put `music/<mood>.mp3` (or `.ogg`) here — moods: `title`, `dusk`, `sunset`, `gloaming`, `blue`, `night`, `dawn`, `deep`. The track loops and replaces the generative score for that mood.
- Effects: put `sfx/<name>.mp3` — names: `tap`, `page`, `type`, `chalk`, `coin`, `unlock`, `card`, `step`, `bell`, `error`, `open`, `close`, `ding`, `stamp`.
- List every file you add in `manifest.json` (a JSON array of relative paths, e.g. `["music/title.mp3", "sfx/bell.mp3"]`). Files not listed are never fetched.

Prompts for Suno / YuE and a search list for Artlist are in `design/12_AUDIO.md`.
