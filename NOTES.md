# Entry notes

Array-board chess engine, deterministic and stdlib-only.

- Full legal move generation (pins, checks, castling, en passant, promotion).
- Iterative deepening alpha-beta with quiescence and a transposition table.
- Tapered piece-square evaluation, bishop pair, killer moves.
- Fixed node budget per iteration (30,000); no clock and no randomness.
- `engine_src.py` is the readable source; `main.py` is made from it with
  `makefun compress`. The fixed node budget keeps every move under the
  10,000 ms per-move limit without reading a clock.
