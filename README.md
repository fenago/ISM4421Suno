# SongForge — AI Music Studio

A single-page app for generating music with the [Suno API](https://docs.sunoapi.org). It's one static `index.html` with no build step and no backend.

## Features
- **Simple mode**: describe a song and pick a style. Suno writes the lyrics and produces 2 variations.
- **Custom mode**: your own title, lyrics and style, plus excluded styles, vocal gender, target length (10–360s), style adherence, weirdness and variety.
- **AI lyric writer**: generates lyric drafts from a short theme and fills them into the composer.
- **Instrumental toggle** and a model picker (V6, V6 Wild, V6 Mini).
- **Live progress**: you can stream the first take before the final files are ready. In-progress jobs pick up again after a page reload.
- **Library** saved in the browser: play, search, download MP3, convert and download WAV, **extend** a track from any point, view or reuse lyrics, copy the audio link, delete.
- A remaining-credits display in the header.

## API key
Each user brings their own Suno API key (get one at https://sunoapi.org/api-key).
The app asks for the key on first use and stores it only in that browser's `localStorage`. The browser sends it straight to `api.sunoapi.org`.

## Deploy to Netlify
1. Connect this repo in Netlify (or drag the folder into Netlify Drop).
2. Leave the build command empty. The publish directory is `.`, which `netlify.toml` already sets.

To run locally, serve the folder with any static server, e.g. `npx serve .`.

> Note: Suno keeps generated files for 14 days, so download the tracks you want to keep.
