NUVORI MISSIONS — BRAND ASSET UPGRADE (v5)
==========================================

WHAT CHANGED
- Hero emblems on BOTH pages now use the true-transparent emblem asset
  (assets/NUVORI_emblem_gold_transparent.png), not the embossed-on-dark
  baked version. This removes the faint dark disc on the mission page —
  the emblem now floats clean on obsidian with zero disc by construction.
- All inline base64 hero data-URIs removed -> asset-path build.

FILE SIZES
- 01-daily-routine/index.html : ~122 KB  ->  ~41 KB
- index.html (landing)        :  ~37 KB  ->   ~8 KB

ASSET SET (assets/)
- NUVORI_emblem_gold_transparent.png   1024x1024 RGBA (real alpha)
- NUVORI_wordmark_gold_transparent.png 2000x367  RGBA (real alpha)
- NUVORI_footer_mark_gold_transparent.png 256x256 RGBA
- NUVORI_favicon_128.png 128x128 RGBA
- NUVORI_app_icon_512.png 512x512 (emblem on obsidian ground)
- NUVORI_og_card.jpg 1200x630 (emblem + wordmark + tagline, for WhatsApp unfurl)

VERIFICATION (tr-TR mobile gate, 390x844 @2x, 900ms wait)
- I-bug hits: 0 on both pages
- Broken images: 0 on both pages
- Disc: none (emblem alpha verified transparent; corners alpha=0)

NOTE ON EMBLEM SOURCE
- The transparent emblem was reconstructed from the checkerboard proof
  (ChatGPT's transparent export arrived flattened to RGB in transit).
  Clean and disc-free at all sizes used here (<=300px). If a texture-perfect
  master is needed for large/print formats, re-supply the flat-black emblem
  PNG and it can be re-keyed losslessly.

DEPLOY
- .nojekyll present. CNAME.txt staged for missions.nuvori.com (rename to
  CNAME when the domain is pointed).
