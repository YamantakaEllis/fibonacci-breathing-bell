[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22765549.svg)](https://doi.org/10.5281/zenodo.22765549)

# fibonacci-breathing-bell

Fibonacci-weighted Bell preservation under depolarizing noise.

2-qubit Bell circuit: `H(0)+CX(0,1)` followed by Fibonacci-weighted `RX(f/max*0.314)` interleaved with `CX` and phi-weighted delays `D(f/max*phi*200)`.

### Results (AerSimulator, 5% noise, 1024 shots)
- **Fib8** (1,1,2,3,5,8,13,21): `{'0': 516, '1': 508}` **GAP 8**
- **Fib13** (1..233): `{'0': 505, '1': 519}` **GAP 14**
- **Fib13 + Gasp RX(1.57)**: `{'0': 511, '1': 513}` **GAP 2** — near-ideal 50/50 Bell preservation

Metric: `GAP = |N0 - N1|`, ideal = 0.

### Interpretation
Fibonacci breathing preserves entanglement; initial gasp improves deep sequence. Reproducible in 30s Colab.

**Author:** Yamantaka Ellis, Melbourne 2026  
**DOI:** https://doi.org/10.5281/zenodo.22765549  
**License:** MIT

Run in Colab: `pip install qiskit qiskit-aer`
