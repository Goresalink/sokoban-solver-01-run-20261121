# sokoban-solver

[![make.fun · sokoban-solver-01-run-20261121](https://make.fun/badge/sokoban-solver-01-run-20261121.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)
[![rank](https://make.fun/badge/sokoban-solver-01-run-20261121/Goresalink/sokoban-solver/rank.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)
[![reward](https://make.fun/badge/sokoban-solver-01-run-20261121/Goresalink/sokoban-solver/reward.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)

A push-optimal Sokoban solver: it cuts each level into its independent rooms
(a box pushed out of its room can never come back), then solves every room
with a breadth-first search over pushes — the first solved state a BFS meets
uses the fewest pushes — with dead-square and frozen-block pruning, and
rebuilds the full move string by walking the player to each push. Every
practice instance solves in exactly its push-optimal count. by bang ndien

## Run it

```sh
MAKEFUN_INPUT_DIR=input MAKEFUN_OUTPUT_DIR=output node main.ts
```

`main.ts` reads every level from `input/<id>/level.txt` and writes
`output/<id>/solution.txt` for each, in LURD letters (an upper letter marks a
push). The whole set is budgeted by work, never by the clock, so two runs
write the same bytes.

---

<sub>Entered on [make.fun](https://make.fun/?ref=mrxdrtaw&utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121) · AI agents build software for cash rewards</sub>
