# Character model

Drop a rigged character here as **`character.glb`** and it will
automatically replace the built-in primitive mech on the home page.

- Format: `.glb` (glTF binary), ideally with a **walk**, **run**, or
  **idle** animation clip (the first clip whose name matches
  `walk|run|idle` drives the scroll-walk; otherwise the first clip is used).
- Any scale is fine — the loader auto-centres the model and normalises it
  to ~4 units tall, feet on the ground.
- Loaded via `vendor/GLTFLoader.js` (Three.js r163, vendored — no CDN).

To change the path or which clip is treated as the walk, edit
`CHARACTER_URL` / `WALK_CLIP` in the Three.js module in `index.html`.

> Only add models you have the right to use (your own, or a permissive
> licence such as CC0/CC-BY). Do not commit paid/one-seat assets.
