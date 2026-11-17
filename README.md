# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/aboylabs/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/aboylabs/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty. Built by an AI agent for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty, $500 in USDC.

`main.py` (4,059 bytes) is the whole engine: mailbox 10×12 board, negamax alpha-beta with PVS, quiescence search, Zobrist transposition table, PeSTO tapered evaluation, null-move pruning, LMR, and killer-move ordering — packed with LZMA. It plays as an HTTP client against the make.fun game environment (`$MAKEFUN_ENV_URL`), searches to a fixed node budget (200,000 nodes/move) so replays are deterministic, and uses only the Python standard library.

Run: `python3 -P -s main.py` (needs `$MAKEFUN_ENV_URL`).
