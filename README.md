# 🧠 When Two Quantum States Meet: Measuring Overlap with the SWAP Test

### A Hands-On Quantum Fidelity Lab Built with Qiskit AND Pennylane

---

## 🧩 Overview

How do we measure *how close* two quantum states are — when they exist in superposition and can’t be directly observed?

This project, **"The Quantum Fidelity Lab"**, explores that question using **Qiskit** and the **SWAP test**, a core quantum algorithm for estimating **state overlap (fidelity)** between two quantum states.

We construct quantum circuits, simulate measurements, and visualize how quantum states change on the **Bloch sphere**, bridging geometric intuition and quantum probability.

---

## 🎯 Project Goal

Measure and understand **quantum fidelity**  
\[
F = |\langle \psi | \phi \rangle|^2
\]
as a function of rotation between two qubit states, and confirm its theoretical relationship:
\[
F = \cos^2\!\left(\frac{\Delta\theta}{2}\right)
\]

---

## ⚙️ Features

✅ Prepare single-qubit states with arbitrary rotations (RY, RZ)  
✅ Compute analytic and measured fidelities  
✅ Implement the **SWAP test** for experimental fidelity estimation  
✅ Visualize states on the **Bloch sphere**  
✅ Plot fidelity vs. angle — observe smooth \(\cos^2\) behavior  
✅ Connect results to **quantum kernel** concepts used in QML  

---

## 🧠 Background

In quantum computing, **fidelity** measures how similar two states are.  
- \( F = 1 \) → identical states  
- \( F = 0 \) → orthogonal (completely different) states  

The **SWAP test** uses an *ancilla qubit* to determine this overlap by controlling whether two states are swapped or not, and then observing interference on the ancilla.  
The probability of measuring `0` on the ancilla is directly related to fidelity:
\[
P(0) = \frac{1 + |\langle \psi | \phi \rangle|^2}{2}
\]

---

## 🧰 Tools & Libraries

- 🧱 **Qiskit** — for circuits, state simulation, and visualization  
- ⚙️ **Qiskit AerSimulator** — for shot-based simulations  
- 📊 **Matplotlib** — for plotting fidelity curves  
- 🔢 **NumPy** — for parameter control and math  

---

## 🧪 Workflow

1. **State Preparation:**  
   Create two qubit states \( |\psi\rangle \) and \( |\phi\rangle \) using controlled rotations.

2. **Analytic Fidelity:**  
   Compute fidelity using Qiskit’s `state_fidelity()` from `qiskit.quantum_info`.

3. **SWAP Test Circuit:**  
   Build a 3-qubit circuit:
   - Ancilla in \(|+\rangle\)
   - Controlled-SWAP between two target qubits
   - Measure ancilla to estimate fidelity

4. **Parameter Sweep:**  
   Vary the rotation angle \( \theta' \) and observe how fidelity changes.

5. **Visualization:**  
   Plot fidelity vs. \( \theta' \) and compare analytic vs. SWAP-test results.

---

## 📈 Results

- The experimental SWAP-test fidelities closely matched analytic values.  
- Fidelity followed the expected \(\cos^2(\Delta\theta / 2)\) curve.  
- Visualizing states on the Bloch sphere showed their geometric separation clearly.  

| State Relationship | Expected Fidelity | Observation |
|---------------------|------------------|--------------|
| Nearly identical    | ≈ 1.0            | Ancilla ≈ always 0 |
| 90° apart           | ≈ 0.5            | Mixed counts |
| Opposite direction  | ≈ 0.0            | Ancilla 0/1 equally likely |

---

## 💡 Key Takeaways

- Fidelity quantifies *how much two quantum states “agree.”*  
- The SWAP test converts that overlap into a measurable probability.  
- These ideas form the **foundation for quantum kernels** in quantum machine learning (QML).  

---

## 🧑‍💻 How to Run

```bash
# Clone this repository
git clone https://github.com/<your-username>/quantum-fidelity-lab.git
cd quantum-fidelity-lab

# Install dependencies
pip install qiskit matplotlib numpy

# Open the notebook
jupyter notebook Quantum_Fidelity_Lab.ipynb
