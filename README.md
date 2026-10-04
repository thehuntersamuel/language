# Language Split

A four-session language rotation (Load, Reps, Speak, Field) with spaced-repetition cards.
German and Japanese decks are built in. Progress saves in the browser, and syncs across devices once you sign in.

Live at https://thehuntersamuel.github.io/language/

- `index.html` is the whole app.
- `audio/` holds one voice clip per card, named by card id, plus `manifest.json` listing which clips exist.
  Cards without a clip fall back to the browser's built-in voice.
- `vendor/supabase.js` is the Supabase browser library (v2.117.2), shipped with the site so it has no third-party runtime dependency.
- Sync uses two tables, `language_progress` and `language_decks`, locked by row security to the signed-in owner.
  The key in `index.html` is a publishable key and is meant to be public.
