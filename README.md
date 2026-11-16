# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/museng1/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/museng1/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python for the [tiny-chess-01](https://make.fun/bounty/tiny-chess-01) bounty on [make.fun](https://make.fun).

`main.py` is the whole engine (packed by `makefun compress` from a
readable source kept beside the repository during the build). It plays
the env's gauntlet of eight house engines over the env API: negamax
alpha-beta search on a 0x88 board with a transposition table,
quiescence search over captures, promotions and check evasions,
null-move pruning, late-move reductions, check extensions, MVV-LVA /
killer move ordering, and a tapered material + piece-square
evaluation with the bishop pair. Every move is chosen under a fixed
node budget that shrinks as the game lengthens — never by a clock —
so a trial replays move for move.
