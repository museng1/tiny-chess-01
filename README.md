# tiny-chess-01

A chess engine in 4 KB of Python for the make.fun tiny-chess-01 bounty.

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
