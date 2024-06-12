# Conversion-of-quantum-expectation-value-problem-to-classical-deep-learning-problem
Conversion of quantum expectation value problem using shadow tomography to deep learning problem by doing fewer measurement 

This project is part of the thesis work of the undergraduate course. In this project, I used quantum shadow tomography to get a succinct classical description of unknown quantum many-body states by repeated measurement using **Variational quantum eigensolver (VQE)**. Then, I used classical **machine learning and deep learning algorithms** to predict **expectation values from Pauli operators and coefficients**. However, previous work in this domain uses **hybrid quantum machine learning** to predict expectation value and other properties of objects like Rényi entropy. Moreover, in this task, I used classical machine learning to see if it is possible to **decrease RMSE errors using only 186 measurements**, whereas in previous work, the **authors used 1500 measurements**.

Papers work I have extended:
1) **Predicting many properties of a quantum system from very few measurements (https://www.nature.com/articles/s41567-020-0932-7)**
2) **Efficient estimation of Pauli observables by derandomization (https://arxiv.org/abs/2103.07510)**
3) **Information-theoretic bounds on quantum advantage in machine learning (https://www.arxiv.org/abs/2101.02464)**

The code of the original papers is hosted on the following links

1) https://github.com/hsinyuan-huang/predicting-quantum-properties
2) https://github.com/renatawong/classical-shadow-vqe

Quick guide for some necessary tutorials for this work

1) https://www.youtube.com/watch?v=NXejv2wVwas
2) https://www.classiq.io/algorithms/variational-quantum-eigensolver-vqe
3) https://qiskit-community.github.io/qiskit-nature/tutorials/06_qubit_mappers.html
4) https://www.youtube.com/watch?v=YtepXvx5zdI
