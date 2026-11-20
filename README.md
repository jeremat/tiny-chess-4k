# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/jeremat/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/jeremat/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python (3,580 bytes, packed from a readable source with `makefun compress`): 0x88 board, alpha-beta search with a transposition table, killer moves, null-move pruning, late-move reductions, check extensions and quiescence search with delta pruning, with a tapered piece-square evaluation (material, piece-square tables, bishop pair, tapered king). It plays the make.fun house gauntlet through the env at MAKEFUN_ENV_URL, to a fixed budget of 50,000 nodes per move, never a clock, never any randomness.

## Practice results

Local practice trials against the house gauntlet (6 games each, deterministic):

- trial-0: **Elo 1545** — 4 wins, 1 draw, 1 loss, including a win against the nodes-500k anchor
- trial-1: **Elo 1279** — 3 wins, 3 losses
- mean **Elo 1412**, above the 1,154 practice floor and above the sunfish reference engine's practice mean (~1,365)

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=frda4ek8&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
