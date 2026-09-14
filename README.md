# Deep Bhakti

A minimal, single-file devotional meditation app. Guides the practitioner inward, progressively disappears, and gently brings them back — no backend, no build step, just `index.html`.

60-minute structure: Settle → Mantra + Breath → Līlā-smaraṇa (Govardhana) → Akṣara-dhyāna → Silence → Return. A 60-second preview mode is available on the setup screen for quickly checking the full flow.

Bells and ambient rain are synthesized in the browser with the Web Audio API — no audio files to source or host.

## Run locally

Just open `index.html` in a browser, or serve it:

```
npx serve .
```

## Host on GitHub Pages

1. Push this folder to a GitHub repo (root of the repo, or a `/docs` folder — either works).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch", pick the branch and the folder (`/root` or `/docs`).
4. Save. GitHub will publish it at `https://<username>.github.io/<repo>/` within a minute or two.

`.nojekyll` is included so GitHub Pages serves the file as-is without running it through Jekyll.

## Notes

- All timing is timestamp-based (`Date.now()`), so the session survives tab-backgrounding/throttling correctly — reopening a stale tab immediately jumps to the correct phase and elapsed time.
- Settings (voice guidance, ambient sound, preview mode) persist in `localStorage`.
- The Govardhana scene and Rādhā-Kṛṣṇa lotus-feet image are text placeholders — swap in real artwork by replacing the `.lila-image-holder` and `.breath-image` contents in `index.html`.
