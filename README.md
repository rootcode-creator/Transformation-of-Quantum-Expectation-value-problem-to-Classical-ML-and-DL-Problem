<h1 align="center">Transformation of Quantum Expectation Value Problem to Classical ML/DL Problem</h1>

<p align="center"><i>Quantum shadow tomography + VQE data generation + classical machine learning/deep learning for expectation value prediction.</i></p>

<p align="center">
	<img src="https://img.shields.io/badge/PROJECT-THESIS-E11D48?style=for-the-badge&labelColor=7F1D1D" alt="Thesis project" />
	<img src="https://img.shields.io/badge/STATUS-ACTIVE-84CC16?style=for-the-badge&labelColor=14532D" alt="Active" />
	<img src="https://img.shields.io/badge/DOMAIN-QUANTUM%20ML-8B5CF6?style=for-the-badge&labelColor=4C1D95" alt="Quantum ML" />
	<img src="https://img.shields.io/badge/LICENSE-RESEARCH-0EA5E9?style=for-the-badge&labelColor=1E3A8A" alt="Research use" />
</p>

<p align="center">
	<img src="https://img.shields.io/badge/PYTHON-3.x-14B8A6?style=for-the-badge&logo=python&logoColor=white&labelColor=0F766E" alt="Python" />
	<img src="https://img.shields.io/badge/QISKIT-QUANTUM-6366F1?style=for-the-badge&logo=qiskit&logoColor=white&labelColor=4338CA" alt="Qiskit" />
	<img src="https://img.shields.io/badge/PANDAS-DATA-06B6D4?style=for-the-badge&logo=pandas&logoColor=white&labelColor=155E75" alt="Pandas" />
	<img src="https://img.shields.io/badge/SCIKIT--LEARN-ML-A855F7?style=for-the-badge&logo=scikitlearn&logoColor=white&labelColor=7E22CE" alt="Scikit-learn" />
	<img src="https://img.shields.io/badge/CATBOOST-MODELING-F59E0B?style=for-the-badge&labelColor=92400E" alt="CatBoost" />
</p>

## Project overview

This repository contains undergraduate thesis work focused on converting a **quantum expectation value estimation problem** into a **classical ML/DL prediction problem**.

Main idea:
- Use **quantum shadow tomography** to build a compact classical representation of many-body quantum states.
- Generate measurement datasets from VQE-based setups.
- Train classical machine learning/deep learning models to predict expectation values from Pauli observables and coefficients.
- Evaluate whether strong prediction can be achieved with significantly fewer measurements (e.g., around 185) compared with larger baselines used in prior work.

## Table of contents

- [Project overview](#project-overview)
- [Repository structure](#repository-structure)
- [Workflow](#workflow)
- [How to run](#how-to-run)
- [Key files](#key-files)
- [Extended papers](#extended-papers)
- [Reference implementations](#reference-implementations)
- [Learning resources](#learning-resources)

## Repository structure

```txt
.
├── Classical Machine learning and Deep learning/
│   ├── V13/
│   ├── V14/
│   │   ├── WITH SMAGON/
│   │   └── WITHOUT APPLYING SMAGON/
│   └── V16/
│       ├── WITH SMAGON/
│       └── WITHOUT APPLYING SMAGON/
├── Derandomize Quantam Shadow Tomography/
│   ├── V4/
│   │   ├── CLASSICAL SHADOW/
│   │   └── DERANDOMIZE CLASSICAL SHADOW/
│   └── V6/
└── README.md
```

## Workflow

1) **Generate / design measurement procedures**
- Randomized classical shadow and derandomized shadow variants.

2) **Acquire shadow-based data**
- Produce measurement operators/outcomes and expectation-related datasets.

3) **Train classical ML/DL models**
- Use generated classical datasets (CSV files) to train and evaluate predictive models.

4) **Compare configurations**
- Compare versions (`V13`, `V14`, `V16`) and experiment branches (with/without SMAGON).

## How to run

> The project is experiment-driven across multiple folders/versions. Run scripts from the corresponding experiment directory.

Typical steps:

```bash
# 1) Move into a target experiment folder (example)
cd "Classical Machine learning and Deep learning/V13"

# 2) Generate / process measurement procedures or datasets
python data_acquisition_shadow.py

# 3) Run prediction/evaluation flow
python prediction_shadow.py
```

If you are using notebook-based workflows, open and run:
- `electronic_structure_problem_dcs_Hydrozen.ipynb`

## Key files

- `data_acquisition_shadow.py`: shadow measurement procedure generation.
- `modified_derandomization.py`: modified derandomized classical shadow routine.
- `prediction_shadow.py`: expectation value estimation/prediction utilities.
- `Classical_data_H2.csv`, `file1.csv`, `file2.csv`: generated datasets for model training/evaluation.

## Extended papers

1. Predicting many properties of a quantum system from very few measurements  
   https://www.nature.com/articles/s41567-020-0932-7

2. Efficient estimation of Pauli observables by derandomization  
   https://arxiv.org/abs/2103.07510

3. Information-theoretic bounds on quantum advantage in machine learning  
   https://arxiv.org/abs/2101.02464

## Reference implementations

1. https://github.com/hsinyuan-huang/predicting-quantum-properties
2. https://github.com/renatawong/classical-shadow-vqe

## Learning resources

1. https://www.youtube.com/watch?v=NXejv2wVwas
2. https://www.classiq.io/algorithms/variational-quantum-eigensolver-vqe
3. https://qiskit-community.github.io/qiskit-nature/tutorials/06_qubit_mappers.html
4. https://www.youtube.com/watch?v=YtepXvx5zdI
