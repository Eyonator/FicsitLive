# Translations

Each file is one language: `<language code>.json`, for example `en.json` or `nl.json`. Every language has the same keys; `en.json` is the fallback for any key a language does not have yet.

`en.json` and `nl.json` here are updated with every release, so they always hold the texts of the newest version.

## Add a language

1. Copy `en.json` and name the copy after your language code: `de.json`, `fr.json`, `pt-BR.json`.
2. Translate the values. Leave the keys as they are.
3. `{words in braces}` are filled in by the app, such as `{version}` or `{seconds}`. Keep them, even where your language puts them in another place in the sentence.
4. Keep the file valid JSON: straight double quotes around every key and value, a comma between entries, and `\"` for a quote inside a text.

## Try it in the app

Put your file in a folder of your own. In FICSIT Live, open **Settings**, set **Folder with translations** to that folder and confirm the short restart of the bridge. Your language appears in the language menu at the top right. You can keep editing the file while FICSIT Live runs: the dashboard picks up every save.

## Share it

Open a pull request that adds `locales/<code>.json`. Once it is accepted, it ships with the next release. When a new version adds keys, they show in English until someone translates them; a pull request that fills them in is just as welcome.

---

# Vertalingen

Elk bestand is één taal: `<taalcode>.json`. Alle talen hebben dezelfde sleutels; `en.json` is de terugval voor een sleutel die een taal nog niet heeft. `en.json` en `nl.json` hier worden bij elke release bijgewerkt. Een nieuwe taal: kopieer `en.json`, noem hem naar de taalcode, vertaal de waarden, laat de sleutels en `{woorden tussen accolades}` staan, en open een pull request met `locales/<code>.json`.
