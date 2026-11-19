# _source

Full-resolution originals behind the optimised files in `assets/`.

- `images/` - AI-generated source images (Gemini), as exported. `*_new` files are later variants of `brine`, `dhi`, `fizz` and `salt`; the live site uses the optimised 1920x1080 JPGs in `assets/img/`.
- `music/` - original track before normalisation (live copy: `assets/music.mp3`). Keep the licence/download page record next to it.

The leading underscore keeps this folder out of the GitHub Pages build (Jekyll skips `_` folders), so these files are not served at deepsignals.tech. If a `.nojekyll` file is ever added, move this folder out of the repo first.
