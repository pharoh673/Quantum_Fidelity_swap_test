# Quantum_Fidelity_swap_test
Understand and measure how similar two quantum states are using fidelity and the SWAP test.

This notebook is a quantum fidelity experiment built in Qiskit.

Goal:
Quantify how similar two quantum states are using the fidelity measure

$$ F=∣⟨ψ∣ϕ⟩∣2 $$

and verify it experimentally through the SWAP test.

Includes:

Single-qubit state preparation and Bloch-sphere visualization

Analytic vs. measured fidelity comparison

Fidelity vs. angle sweep showing 
$$ cos⁡2(Δθ/2) $$
relationship

Step-by-step code and circuit visualization

Outcome:
A clear, hands-on understanding of quantum state similarity — the foundation for quantum kernels and future QML models.

Installation

1️⃣ Create a virtual environment python -m venv qml_env 

2️⃣ Activate it

Windows: qml_env\Scripts\activate

macOS / Linux: source qml_env/bin/activate 
3️⃣ Install dependencies pip install jupyterlab numpy matplotlib seaborn scikit-learn pip install qiskit qiskit-aer qiskit-machine-learning qiskit-algorithms

4️⃣ Launch Jupyter jupyter lab

