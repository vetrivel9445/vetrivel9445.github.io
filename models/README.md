# Character model

## Your own 3D cartoon avatar → `avatar.glb`

Want the character in the pod to be a **3D cartoon of you**? Generate one and
save it here as **`avatar.glb`** — the site detects it on load and uses it
automatically (keeping its real colours, not the cyan wireframe). No code
changes needed. If the file isn't present, the site falls back to the default
hologram figure.

**How to make one (free, ~2 minutes):**

1. Go to **[readyplayer.me](https://readyplayer.me)** → *Create Avatar*.
2. Choose **"Take a photo"** / upload a selfie — it builds a stylised 3D
   cartoon of your face, then let you pick hair, outfit, glasses, etc.
3. When done, click **Download / Export → `.glb`** (or copy the avatar URL
   ending in `.glb` and download it).
4. Rename the file to **`avatar.glb`** and put it in this `models/` folder,
   then commit & push. Reload the site — it's you in the pod.

Any humanoid `.glb` works (Ready Player Me, Mixamo, VRoid exported to glTF,
Sketchfab CC0, etc.). It's auto-centred and scaled to fit, so size doesn't
matter. Prefer a T-pose / idle model; it rotates slowly on a turntable in the
pod. Keep files reasonably small (RPM avatars are ~1–3 MB).

## Rigged character → `character.glb`

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
