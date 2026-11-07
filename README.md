# Infinite Fusion sprites — #502–576 roster

Auto-generated sprites for the Pokémon Infinite Fusion fan game, covering the
**#502–576** part of the roster. Served over [jsDelivr](https://www.jsdelivr.com/)
and used by [pokemondex.net](https://pokemondex.net).

## Why this repo exists

The community mirror
[`genfusion8/infinite-fusion-graphics`](https://github.com/genfusion8/infinite-fusion-graphics)
is the usual source for these assets, but its auto-generated set stops at
**#501**. It holds:

| path | coverage |
|---|---|
| `custom/*` | complete, including #502–576 |
| `base/1..501`, `triples/*` | complete |
| `autogen/{head}/{head}.{body}.png` | only where **both** ids ≤ 501 |
| `base/502..576` | absent |

This repo fills exactly that gap and nothing else:

| path | files |
|---|---|
| `base/502..576.png` | 75 |
| `autogen/{head}/{head}.{body}.png` where head > 501 or body > 501 | 80,775 |

That is 576² − 501² autogen sprites, about 250 MB. Use the community mirror for
everything else — this repo deliberately does not duplicate it.

## Layout

Identical to the community mirror, so only the host differs:

```
base/{id}.png
autogen/{headId}/{headId}.{bodyId}.png
```

## Usage

```
https://cdn.jsdelivr.net/gh/hashey1000-coder/infinite-fusion-sprites-502-576@main/base/531.png
https://cdn.jsdelivr.net/gh/hashey1000-coder/infinite-fusion-sprites-502-576@main/autogen/531/531.1.png
```

## Credits and provenance

These are **machine-generated** sprites, produced by the Infinite Fusion
project's own autogen process from the game's base sprites — not hand-drawn
community art. Hand-drawn `custom/` sprites are **not** in this repo; they stay
on the community mirror, where their artists are credited.

Pokémon Infinite Fusion is a fan game. Pokémon and all related names are
trademarks of Nintendo / Creatures Inc. / GAME FREAK Inc. This mirror is
non-commercial fan-project infrastructure, provided for convenience only.

## Updating after a new Sprite Pack

Regenerate or re-pull the gap and push. `scripts/fetch-sprite-gap.mjs` in the
pokemondex repo mirrors it, and skips files already present so an interrupted
run resumes:

```
node scripts/fetch-sprite-gap.mjs <out-dir>
```

If a future Sprite Pack raises the roster above #576, bump `MIRROR_MAX_ID` /
`NEW_MAX` there and in `src/lib/spriteConfig.js`.
