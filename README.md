# Quantum Cryptography Research: Keyed Quantum States and Scrambling

Exploratory Python/Qiskit experiments examining keyed quantum-state generation, measurement-limited key recovery, and scrambling-inspired quantum circuits. This is a small-scale research prototype, **not** a secure cryptographic system or a demonstration of quantum-gravity physics.

## Research questions

- How distinguishable are quantum states generated from different 6-bit keys?
- How do limited Z- and X-basis measurements affect recovery of a key?
- Does adding publicly known scrambling layers change key recovery under the tested attacker model?
- How might key-dependent scrambling change these results? (Experiment 7, in progress.)

## Notebook

[`Quantum_Gravity_One_Way_Functions.ipynb`](Quantum_Gravity_One_Way_Functions.ipynb) contains the experiments in order.

| Experiment | Focus |
|---|---|
| 1 | Generate 4-qubit states from a 6-bit key and compare fidelity |
| 2 | Exhaustively compare 64 candidate keys using ideal statevectors |
| 3 | Evaluate key recovery from 100 simulated Z-basis measurement shots |
| 4 | Combine 100 Z-basis and 100 X-basis shots |
| 5–6 | Test public scrambling layers and key recovery at several depths; examine reversibility |
| 7 | Begin key-dependent scrambling model (**in progress**) |

## Methods and limitations

Experiments use Qiskit statevector simulation, NumPy, and Matplotlib. The attacker is restricted differently across experiments; ideal-statevector access and finite-shot measurement access are not equivalent. The key space is only 64 candidates, and the circuits use four qubits. Findings are exploratory and do not establish cryptographic one-wayness, security, or quantum advantage. Public unitary scrambling is reversible when its circuit is known.

The notebook includes code for a 30-trial sweep over five scrambling depths (150 trials total); rerun it to reproduce numerical results. The uploaded copy intentionally has no stored outputs.

## Running

Open the notebook in Google Colab and execute cells in order. The notebook installs Qiskit, NumPy, and Matplotlib.

## Research status

Independent exploratory experiments. Experiment 7 remains unfinished. This repository is distinct from any unpublished or restricted faculty-led research materials.
