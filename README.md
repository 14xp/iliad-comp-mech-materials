# Iliad — Computational Mechanics Materials

ARENA-style, hands-on exercises for the computational-mechanics view of sequence
models: you implement a hidden Markov model (HMM) from scratch and watch its
**next-token** and **belief-state** geometry emerge.

## HMM from scratch

Two parts. Each has an **exercises** notebook (with `# YOUR CODE HERE` stubs,
inline tests, and collapsible solutions) and a fully worked **solutions** notebook.

| Notebook | Open in Colab |
| --- | --- |
| **Part 1 — Sequence probabilities & next-token distributions** (exercises) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/14xp/iliad-comp-mech-materials/blob/main/exercises/colab/part1_sequence_probabilities_exercises_colab.ipynb) |
| Part 1 (solutions) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/14xp/iliad-comp-mech-materials/blob/main/exercises/colab/part1_sequence_probabilities_solutions_colab.ipynb) |
| **Part 2 — Belief states** (exercises) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/14xp/iliad-comp-mech-materials/blob/main/exercises/colab/part2_belief_states_exercises_colab.ipynb) |
| Part 2 (solutions) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/14xp/iliad-comp-mech-materials/blob/main/exercises/colab/part2_belief_states_solutions_colab.ipynb) |

The Colab notebooks are **self-contained** — their Setup cells write the helper
modules into the session, so there's nothing else to install or download. Just
open in Colab (Python 3.12) and run top to bottom.

## Running locally

The notebooks under [`exercises/`](exercises/) (the non-`colab/` ones) run
in any Jupyter environment with **Python 3.12**:

```bash
pip install -r requirements.txt        # or: uv venv && uv pip install -r requirements.txt
cd exercises
jupyter lab
```

Work through `part1_sequence_probabilities_exercises.ipynb` then
`part2_belief_states_exercises.ipynb`. Fill in each `# YOUR CODE HERE` cell and run
its `tests.test_*(HMM)` cell — it prints **All tests passed!** when correct.

## How the notebooks are built

Everything is generated from a single source of truth by
[`exercises/build_notebooks.py`](exercises/build_notebooks.py): per-cell
prose (`prose.json`), the reference implementation (`solutions.py`), the tests
(`tests.py`), and the example processes (`processes.py`) / plotting (`plotting.py`).
To regenerate all eight notebooks (local + Colab) after editing any of those:

```bash
cd exercises
python build_notebooks.py
```
