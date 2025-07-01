# PINs and Semi-PINs: An Experimental Inquiry into Number Theory

This repository contains the research, data, and Python code for an experimental number theory project exploring the structure of composite numbers based on their proximity to primes. We introduce and analyze two novel classes of numbers:

-   **Pseudo-Isolated Numbers (PINs):** Composite numbers `n` that are the center of a twin prime pair (`n-1` and `n+1` are both prime).
-   **Semi-Pseudo-Isolated Numbers (Semi-PINs):** Multiples of 6 that have exactly one prime neighbor.

## Core Concepts & Discoveries

This project moves beyond simple classification to uncover deep structural patterns. The key findings, supported by numerical experiments up to $5 \times 10^7$, include:

1.  **A Fundamental Partition:** PINs and Semi-PINs are proven to be **disjoint sets**. Together, they form the complete neighborhood for all prime numbers greater than 3.

2.  **The Factorization Shielding Principle:** We discovered that the likelihood of a number being a PIN or Semi-PIN is strongly correlated with its "atomic structure" (prime factorization). Numbers divisible by many small, distinct primes (e.g., 2, 3, 5, 7) are far more likely to have prime neighbors. This is because they "shield" their neighbors from these common divisions.

3.  **Construction and Failure Analysis:** We developed algorithms to actively construct these numbers by building them from a "primorial core" (like `2*3*5*7 = 210`). This method has a remarkable success rate of **~43%**. We further analyzed the failures, showing they are not random but are governed by predictable congruence classes, providing a clear illustration of the Chinese Remainder Theorem in action.

## Repository Structure


-   **/code/**: Includes the Python scripts used for number generation, analysis, and visualization. The code is commented to explain the implementation of each experiment.
-   **/data/**: Raw data files and results from large-scale computational runs.
-   **/visualizations/**: Key graphs and plots, including the "Primality Energy Landscape" which provides an intuitive model of the concepts.

## How to Use

To replicate the experiments, you will need Python 3 with the `matplotlib` and `numpy` libraries. All core algorithms are contained in the `analysis_code.py` file. You can run it directly to generate results for a given search limit.
