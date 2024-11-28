# Secure-quantum-key-distribution-using-the-BB84-protocol

Overview:
This repository contains an implementation of the BB84 protocol for secure quantum key distribution (QKD). The BB84 protocol, introduced by Charles Bennett and Gilles Brassard in 1984, uses quantum mechanics to enable two parties (Alice and Bob) to securely exchange cryptographic keys over an insecure channel. The protocol relies on the fundamental principle that observing quantum states disturbs them, ensuring the secrecy of the exchanged key.

The implementation here simulates the quantum process, showing how quantum states (qubits) are transmitted, measured, and reconciled to form a secure key. The project leverages Python libraries like Qiskit for quantum computing simulations.

Key Features:
Quantum Secure Communication: Demonstrates quantum key distribution using the BB84 protocol.
Quantum Circuit Simulation: Uses the Qiskit framework to simulate quantum gates, entanglement, and measurement of qubits.
Key Exchange Visualization: Visualizes the key exchange process and compares bases between Alice and Bob.
Eavesdropping Detection: Simulates the effect of eavesdropping on the quantum channel.
Table of Contents
Introduction
Protocol Steps
Setup Instructions
Usage
How It Works
Eavesdropping Detection
Future Work
Contributing
License
Introduction
The BB84 protocol enables two parties, Alice (the sender) and Bob (the receiver), to securely exchange a cryptographic key. The protocol uses quantum mechanics to ensure the security of the exchanged key by leveraging the principle that any attempt by a third party (Eve, the eavesdropper) to measure or intercept the quantum bits (qubits) will disturb the communication and be detectable.

In this implementation, you will see how quantum states are prepared, transmitted, and measured:

Alice prepares qubits in one of four states: two for the computational basis (0, 1) and two for the diagonal basis (±).
Bob measures the qubits using randomly chosen bases.
The shared key is constructed by comparing bases over a classical channel and discarding bits where the bases did not match.
Protocol Steps
Initialization: Alice prepares a sequence of qubits in either the computational or diagonal basis.
Transmission: Alice sends the qubits through the quantum channel to Bob.
Measurement: Bob measures the qubits, using a randomly chosen basis.
Basis Reconciliation: Alice and Bob compare their bases over a classical channel, and discard bits where the bases did not match.
Key Extraction: The remaining bits form the shared secret key.
The quantum states used in BB84:
0 (computational basis): |0⟩
1 (computational basis): |1⟩
+ (diagonal basis): (|0⟩ + |1⟩)/√2
− (diagonal basis): (|0⟩ − |1⟩)/√2
Setup Instructions
To run the notebook and simulate the BB84 protocol, follow these instructions:

Prerequisites:
Python 3.x installed.
The following Python libraries:
Qiskit (for simulating quantum operations)
matplotlib (for visualizations)

Installation:
Clone the repository:
git clone https://github.com/ABR-2005/Secure-quantum-key-distribution-using-the-BB84-protocol.git
cd Secure-quantum-key-distribution-using-the-BB84-protocol
Install the required dependencies:
pip install -r requirements.txt

Usage:
Open the Jupyter Notebook:
To open the notebook in Jupyter, navigate to the folder containing the repository and run:
bash
Copy code
jupyter notebook BB84_protocol_implementation.ipynb
In the notebook:
Step through the code to simulate Alice and Bob’s quantum key distribution process.
View the results of key reconciliation and measurement in visual form.
