# AG1

A proof is a chain of blocks: **given facts → block → block → … → goal**.

Covered so far: Lectures 1, 2, 3, 4, 12 — 216 facts, 189 blocks.

## Files

| File | What it is |
|---|---|
| `graph.html` | Graph theory: start from a fact a statement gives you and open the blocks step by step, with the formal proof along each path. The sidebar lists every definition block and fact block. Open it in a browser. |
| `algorithms.html` | Algorithms and data structures: one interactive page per algorithm or data structure (Lectures 1–12), grouped by topic, with pseudocode and review notes. |
| `blocks/blocks-lecture-01.md` | 58 blocks first introduced in Lecture 1 |
| `blocks/blocks-lecture-02.md` | 44 blocks first introduced in Lecture 2 |
| `blocks/blocks-lecture-03.md` | 38 blocks first introduced in Lecture 3 |
| `blocks/blocks-lecture-04.md` | 40 blocks first introduced in Lecture 4 |
| `blocks/blocks-lecture-12.md` | 9 blocks first introduced in Lecture 12 |
| `blocks/frames.md` | 11 Frame blocks (first and last line of a proof) |
| `blocks/techniques.md` | 11 Technique blocks (contradiction, pigeonhole, …) |
| `index/by-needs.md` | “I have this fact” → blocks that accept it |
| `index/by-gives.md` | “I want this fact” → blocks that produce it |

## How to solve a problem

1. **Frame.** Look at the form of the question and take the frame from `frames.md`.
2. **Given.** List every fact in the statement. Look each one up in `by-needs.md` (or click it in `graph.html`) and write down what it gives.
3. **Goal.** Look up the fact you must reach in `by-gives.md` and note what it needs.
4. **Connect.** Work forward from step 2 and backward from step 3 until they meet. If they do not meet, pick a technique from `techniques.md`.
5. **Write.** One Say sentence per block, inside the frame.
