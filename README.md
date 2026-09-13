# $RETIRE

Landing page for **$RETIRE** — a memecoin on Solana.

> Buy a coin. Hold it. Touch grass forever.

Single-page, no build step, no dependencies. Plain HTML, CSS and JavaScript.

## Run it

Open `index.html` in a browser. That's it.

For a local server (optional):

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy on GitHub Pages

1. Push this folder to a repository.
2. Settings → Pages → Source: `Deploy from a branch` → branch `main`, folder `/ (root)`.
3. The site goes live at `https://<user>.github.io/<repo>/`.

`.nojekyll` is included so GitHub serves the files as-is.

## Edit the links

Everything lives in one place. Open `index.html`, search for `EDIT ME`, and edit:

```js
var CONFIG = {
  CA:    "7X8Mdp98VyK64AEJh4qGFYnLngguyMsgqS1kdNtrpump",
  pump:  "https://pump.fun/coin/Hcx8W1TmBQnXEVNWKiPhckP5qVjbCAJ1NpdQV4Q9pump",
  x:     "https://x.com/RetirePumpFun",
  chart: "https://dexscreener.com/solana/Hcx8W1TmBQnXEVNWKiPhckP5qVjbCAJ1NpdQV4Q9pump",
  tg:    "#telegram"
};
```

The contract address, every button, the nav, the footer links and the mobile bar
all read from this object. Leave `CA` empty and the page shows "dropping soon"
instead of an address.

## Social preview image

`og:image` uses a relative path, which most platforms ignore. Once the site is
live, replace it with the full URL:

```html
<meta property="og:image" content="https://your-domain.com/assets/logo.webp">
```

## Structure

```
index.html        markup, styles and scripts
assets/           images (WebP) + favicons
.nojekyll         tells GitHub Pages to skip Jekyll
```

## Notes

- Fonts come from Google Fonts (Instrument Serif + JetBrains Mono). Without a
  network connection the page falls back to Georgia and a system monospace.
- The animated background is a single canvas. It degrades itself on slow
  devices and turns off for `prefers-reduced-motion`.
- Images are pre-compressed WebP. Re-export at the same sizes if you swap them.

## Disclaimer

This is a meme. Not financial advice. Touch grass responsibly.
