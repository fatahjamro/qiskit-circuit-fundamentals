# Qiskit Circuit Fundamentals

> **A structured, hands-on tour of quantum circuits — from single qubits to Quantum Volume.**

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)](https://www.python.org/)
[![Qiskit](https://img.shields.io/badge/Qiskit-2.x-6929C4?logo=qiskit)](https://qiskit.org/)
[![Qiskit Aer](https://img.shields.io/badge/Qiskit--Aer-latest-8a3ffc)](https://qiskit.org/ecosystem/aer/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## Overview

This repository provides a single, clean, fully-runnable Qiskit notebook that builds quantum computing knowledge progressively — from writing a one-qubit circuit to understanding how quantum processors are benchmarked.

All code is written for **Qiskit 2.x** — deprecated APIs (`execute`, `BasicAer`, `assemble`, `FakeVigo`) have been removed and replaced with their modern equivalents.

---

## What You Will Learn

| Section | Topic | Key Concepts |
|---|---|---|
| 1 | Setup | Modern Qiskit 2.x imports |
| 2 | First circuit | Hadamard gate, superposition, circuit drawing |
| 3 | Simulation | AerSimulator, transpile → run workflow, plot_histogram |
| 4 | Entanglement | Bell state, GHZ state, CNOT gate |
| 5 | Registers & Toffoli | QuantumRegister, ClassicalRegister, multi-control gates |
| 6 | State visualisation | DensityMatrix, partial_trace, plot_state_city |
| 7 | Parametrised circuits | Parameter class — foundation of VQE |
| 8 | Transpilation | Hardware-native gate decomposition |
| 9 | Batching | Multiple circuits in a single job |
| 10 | Quantum Volume | Benchmarking quantum processor capability |

---

## Quick Start

### Install dependencies

```bash
pip install qiskit qiskit-aer numpy matplotlib pylatexenc
```

### Clone and run

```bash
git clone https://github.com/fatahjamro/qiskit-circuit-fundamentals.git
cd qiskit-circuit-fundamentals
jupyter notebook qiskit-circuit-fundamentals.ipynb
```

---

## Qiskit API Changes (pre-1.0 → 2.x)

If you have worked with older Qiskit tutorials, note these important changes:

| Old (deprecated) | New (Qiskit 2.x) |
|---|---|
| `from qiskit import Aer` | `from qiskit_aer import AerSimulator` |
| `execute(qc, backend)` | `backend.run(transpile(qc, backend))` |
| `from qiskit.tools.visualization import ...` | `from qiskit.visualization import ...` |
| `BasicAer` | `AerSimulator()` |
| `assemble()` | Not needed — pass circuits directly to `run()` |

---

## Repository Structure

```
qiskit-circuit-fundamentals/
└── qiskit-circuit-fundamentals.ipynb   # Main notebook
```

---

## Series

This notebook is the second in a series building towards variational quantum algorithms:

1. [linear-algebra-for-quantum-computing](https://github.com/fatahjamro/linear-algebra-for-quantum-computing) — Eigenvalues, eigenvectors, and geometric intuition
2. **qiskit-circuit-fundamentals** ← You are here
3. [variational-quantum-eigensolver-vqe](https://github.com/fatahjamro/variational-quantum-eigensolver-vqe) *(coming soon)* — VQE from scratch

---

## About the Author

**Abdul Fatah** — PhD Researcher in Quantum Computing and Computer Science, Atlantic Technological University (ATU) Galway, Ireland.

Specialising in quantum error correction, quantum cryptography, and quantum combinatorial structures. Research recognised by ETH Zurich, Oxford University (NQCC), and published in IEEE QCNC.

- **GitHub:** [github.com/fatahjamro](https://github.com/fatahjamro)
- **LinkedIn:** [linkedin.com/in/fatahjamro](https://linkedin.com/in/fatahjamro)
- **QuantumBeads:** [quantumbeads.com](https://quantumbeads.com)

---

## Licence

MIT — free to use, share, and build upon with attribution.
