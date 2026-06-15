# QCNN Trainability: Absence of Barren Plateaus

## Overview
This repository contains a numerical investigation into the trainability of Quantum Convolutional Neural Networks (QCNNs). It reproduces the core variance-scaling results from the seminal paper ["Absence of Barren Plateaus in Quantum Convolutional Neural Networks"](https://prx.aps.org/abstract/PRX/v11/i4/e041011) (Pesah et al., 2021). 

In standard Variational Quantum Algorithms (VQAs), highly expressive deep circuits naturally form global 2-designs, leading to exponentially vanishing gradients known as "barren plateaus." This project demonstrates that QCNNs do not have barren plateau phenomenon and remaining trainable at scale.

## Key Features
* **Custom Ansatz Design:** Implementation of a highly parameterized 15-parameter, 2-qubit convolutional filter ($W$) and a Controlled-RZ pooling operation.
* **Architectural Comparison:** Dynamically compares the gradient variance of an unstructured (unshared weights) circuit against a structured QCNN (shared weights).
* **Adjoint Differentiation:** Utilizes high-performance state-vector simulation via PennyLane's adjoint differentiation method to efficiently sample gradients across multiple random initializations.
* **Variance Scaling:** Outputs a clear logarithmic visualization of how the gradient variance scales with the number of qubits ($N$), proving polynomial scaling for the shared architecture.

## Technologies Used
* **Framework:** PennyLane 
* **Language:** Python
* **Data Visualization:** Matplotlib / NumPy

## How to Run
To run this notebook locally, ensure you have the required dependencies installed:

```bash
pip install pennylane numpy matplotlib
