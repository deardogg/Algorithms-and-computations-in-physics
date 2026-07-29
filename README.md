# Algorithms and Computations in Physics — MATLAB Solutions

Worked solutions to the problem sheets of *Algorithms and Computations in Physics* (Ylias Sadki & Werner Krauth, University of Oxford, 2025), following W. Krauth, **Statistical Mechanics: Algorithms and Computations** (OUP, 2006; 2nd ed. 2024).

The sheets set the exercises in Python; everything here is implemented from scratch in **MATLAB**.

**Topics:** direct and Markov-chain sampling · Walker's alias method · Metropolis–Hastings · lifted and event-driven (zig-zag) chains · detailed vs. global balance · event-driven molecular dynamics · hard disks and spheres · Hamiltonian Monte Carlo · Lévy construction · matrix squaring and path-integral Monte Carlo · permutation sampling and Bose–Einstein condensation.

---

## Repository layout

Each problem set has a live MATLAB notebook (`.mlx`) with code, output and commentary, plus a `.pdf` export so the work can be read without MATLAB. [`Questions.pdf`](Questions.pdf) contains every question, all four sheets.

```
.
├── Questions.pdf              # all problem sheets, PS1–PS4
├── PS1/
│   ├── PS1.mlx
│   └── PS1.pdf
├── PS2/
│   ├── PS2.mlx
│   └── PS2.pdf
├── PS3/
│   ├── PS3_Q1_event-disks.mlx
│   ├── PS3_Q2_direct-and-markov-disks.mlx
│   ├── PS3_Q3_harmonic-chain.mlx
│   └── PS3.pdf
└── PS4/
    ├── PS4_Q1_matrix-square.mlx
    ├── PS4_Q2_naive-harmonic-path.mlx
    ├── PS4_Q3_three-cycles.mlx
    ├── PS4_Q4_direct-N-bosons.mlx
    └── PS4.pdf
```

---

## Contents

### PS1 — Sampling and convergence
| Question | Algorithm | File |
|---|---|---|
| 1 | `direct-pi` — Monte Carlo estimate of π/4; histogram of estimates against the Bernoulli variance θ(1−θ) | [`PS1/PS1.mlx`](PS1/PS1.mlx) |
| 2 | `walker` — alias-table construction and O(1) sampling from {p₁,…,p_K} | [`PS1/PS1.mlx`](PS1/PS1.mlx) |

### PS2 — Markov chains and balance conditions
| Question | Algorithm | File |
|---|---|---|
| 1 | `markov-pi`; precision vs. throwing range ε; Metropolis–Hastings triangle algorithm for the heliport game | [`PS2/PS2.mlx`](PS2/PS2.mlx) |
| 2 | `metropolis` and `factor-metropolis` on the anharmonic oscillator | [`PS2/PS2.mlx`](PS2/PS2.mlx) |
| 3 | `lifted-metropolis` and the event-driven `zig-zag`; detailed vs. global balance | [`PS2/PS2.mlx`](PS2/PS2.mlx) |

### PS3 — Hard disks and the harmonic chain
| Question | Algorithm | File |
|---|---|---|
| 1 | `event-disks` — event-driven MD; the "batman" projected density for N = 4, σ = 0.15; Maxwell–Boltzmann velocity histogram | [`PS3/PS3_Q1_event-disks.mlx`](PS3/PS3_Q1_event-disks.mlx) |
| 2 | `direct-disks` and `markov-disks`; finite-size deviations at N = 4 | [`PS3/PS3_Q2_direct-and-markov-disks.mlx`](PS3/PS3_Q2_direct-and-markov-disks.mlx) |
| 3 | `levy-harmonic`, `metropolis-harmonic`, `HMC-harmonic`; why the Metropolis step uses U + K | [`PS3/PS3_Q3_harmonic-chain.mlx`](PS3/PS3_Q3_harmonic-chain.mlx) |

### PS4 — Quantum Monte Carlo and bosons
| Question | Algorithm | File |
|---|---|---|
| 1 | `matrix-square` — Trotter decomposition for V = ½x² and V = ½x² + ¼x⁴ | [`PS4/PS4_Q1_matrix-square.mlx`](PS4/PS4_Q1_matrix-square.mlx) |
| 2 | `naive-harmonic-path` — path-integral simulation, harmonic and anharmonic | [`PS4/PS4_Q2_naive-harmonic-path.mlx`](PS4/PS4_Q2_naive-harmonic-path.mlx) |
| 3 | `three-cycles` — uniform sampling of permutations with cycles of length 1, 2, 3 | [`PS4/PS4_Q3_three-cycles.mlx`](PS4/PS4_Q3_three-cycles.mlx) |
| 4 | `direct-N-bosons` — cycle-weight distribution at N = 100; Bose–Einstein condensation vs. N | [`PS4/PS4_Q4_direct-N-bosons.mlx`](PS4/PS4_Q4_direct-N-bosons.mlx) |

---

## Running the code

Open any `.mlx` in MATLAB (R2020b or later; base MATLAB only, no toolboxes required) and run the whole notebook. Each is self-contained — no shared setup file or path configuration. Run times are seconds to a couple of minutes; the boson and hard-disk sweeps are the slowest.

To read the results without MATLAB, open the corresponding `.pdf`.

## Reference

W. Krauth, *Statistical Mechanics: Algorithms and Computations*, Oxford University Press (2006; 2nd ed. 2024). Course materials and the original Python reference implementations are on Werner Krauth's website.
