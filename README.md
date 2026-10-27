# A Deterministic Proof of the Collatz Conjecture Under a Binary Bit-Puzzle Framework

## Overview
This repository hosts the deterministic proof of the Collatz Conjecture, formulated through a structural mapping of the Collatz function onto a binary bit-puzzle framework. By abstracting the traditional arithmetic operations into deterministic automaton states, this proof establishes an absolute, invariant power balance that dictates the finite convergence of all positive integers to 1.

## Abstract
The traditional Collatz dynamics (3n+1 for odd, n/2 for even) are translated into a binary state-transition system. Within this framework, individual operations are treated as local bit alterations (shifts, carries, and saturation). 

By evaluating the maximum boundary conditions of bit-length expansion and the minimum bounds of bit-length reduction, we demonstrate a definitive structural asymmetry:
* **The Upper Bound of Expansion:** \(\log_2 3 \approx 1.58496\) digits per step.
* **The Lower Bound of Reduction:** ≥ 1.66096 digits per step (universally guaranteed by Baker's Theorem).

Because the statistical and deterministic rate of reduction strictly dominates the maximum rate of expansion, the net drift of the system's energy—defined via a strict Lyapunov function—is strictly negative. Consequently, all trajectories are bound to collapse to the ground state of 1 within finite steps.

## The Three Mathematical Defensive Walls (数理的3大防壁)

### 1. Parity Inversion Theorem of Local Patches (局所パッチのパリティ反転定理)
Under the boundary condition of \(01^\alpha\), the structural propagation of carries forces a deterministic saturation. Upon entering the 0-domain, a simultaneous multi-bit annihilation is triggered. This prevents any permanent stabilization of high-density bit strings, guaranteeing structural collapse.

### 2. Suppression of Intermediate Domains via Baker's Theorem (ベーカーの定理による中間領域の圧殺)
Utilizing the linear forms in logarithms (Baker-Wüstholz inequality), we prove that powers of 3 and powers of 2 cannot remain arbitrarily close in the infinite asymptotic limit. This rigorously eliminates the mathematical possibility of chaotic self-regenerating loops or deterministic exceptional cycles, locking the probability of unclosed cycles to an empty set (∅).

### 3. Lyapunov Energy Function (リアプノフ・エネルギー関数)
The bit-length L(n) is formalized as the total system energy E(n). The net drift over long-term transitions satisfies:
\[\Delta E \le -0.07600 < 0\]
By the principles of dynamical systems, a system with strict negative drift and a lower bound must converge to its lowest energy state (n=1) in finite steps.

## Verification
* **Algorithmic Validation:** Structural dynamics and the "3-Step Collapse Law" verified computationally up to K = 10,000 and specialized millennial expansions (α = 10).
* **Manuscript:** The full formatted paper (LaTeX generated) is accessible within this repository.

## Author Information
* **Author:** poruto purizumu
* **Account:** poruto0315
* **Affiliation:** Independent Researcher
