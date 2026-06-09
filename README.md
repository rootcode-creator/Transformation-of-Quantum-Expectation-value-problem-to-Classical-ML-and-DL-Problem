<h1 align="center">Quantum expectation value transformation by machine and deep learning</h1>

<p align="center"><i>Quantum shadow tomography + VQE data generation + classical machine learning/deep learning for expectation value prediction.</i></p>

<p align="center">
	<img src="https://img.shields.io/badge/PROJECT-THESIS-E11D48?style=for-the-badge&labelColor=7F1D1D" alt="Thesis project" />
	<img src="https://img.shields.io/badge/STATUS-ACTIVE-22C55E?style=for-the-badge&labelColor=14532D" alt="Active" />
	<img src="https://img.shields.io/badge/DOMAIN-QUANTUM%20ML-A78BFA?style=for-the-badge&labelColor=4C1D95" alt="Quantum ML" />
	<img src="https://img.shields.io/badge/LICENSE-RESEARCH-38BDF8?style=for-the-badge&labelColor=1E3A8A" alt="Research use" />
</p>

<p align="center">
	<img src="https://img.shields.io/badge/PYTHON-3.x-14B8A6?style=for-the-badge&logo=python&logoColor=white&labelColor=0F766E" alt="Python" />
	<img src="https://img.shields.io/badge/QISKIT-QUANTUM-8B5CF6?style=for-the-badge&logo=qiskit&logoColor=white&labelColor=4338CA" alt="Qiskit" />
	<img src="https://img.shields.io/badge/PANDAS-DATA-06B6D4?style=for-the-badge&logo=pandas&logoColor=white&labelColor=155E75" alt="Pandas" />
	<img src="https://img.shields.io/badge/SCIKIT--LEARN-ML-A855F7?style=for-the-badge&logo=scikitlearn&logoColor=white&labelColor=7E22CE" alt="Scikit-learn" />
	<img src="https://img.shields.io/badge/CATBOOST-MODELING-F59E0B?style=for-the-badge&labelColor=92400E" alt="CatBoost" />
</p>

<h2 id="project-overview" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">📌 Project overview</h2>

This repository contains thesis work on converting a **quantum expectation value estimation problem** into a **classical ML/DL regression problem**. The study uses **NISQ-era quantum computing**, **classical shadow tomography**, and **VQE-generated data** for the H2 molecular system to train models that predict expectation values from compact classical features rather than relying on very large measurement budgets.

In this workflow, the quantum part generates measurement and Pauli-observable data, while the classical part uses ML/DL methods to learn the mapping from those features to expectation values. The result is a practical bridge between quantum chemistry experiments and classical predictive modeling.

> **Quick visual summary**
> - Focus: quantum measurement data → classical expectation-value prediction
> - Domain: H2 molecular system + VQE + shadow tomography
> - Outcome: regression-style ML/DL modeling and experimental comparison
> - Goal: reduce dependence on large measurement budgets while preserving predictive quality

## Table of contents

- [Project overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Installation](#installation)
- [Tools](#tools)
- [Usage](#usage)
- [Results](#results)
- [Project flow](#project-flow)
- [Project structure](#project-structure)
- [Further reading & references](#extended-papers-reference-implementations-and-learning-resources)
- [License](#license)

<h2 id="dataset" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">📊 Dataset</h2>

The datasets in this repository are generated from the H2 quantum chemistry workflow and the classical-shadow measurement pipeline used in the thesis.

- Dataset source: measurement outcomes, Pauli-operator information, and classical-shadow features stored in the experiment folders.
- Main system studied: H2 (with the thesis also comparing related derandomized and VQE-style experiment variants).
- Typical features: Pauli observable information, expectation-value features, coefficient terms, and classical-shadow derived representations.
- Target variable: the expectation value / regression target learned from the generated quantum data.
- Measurement focus: the thesis emphasizes compact measurement settings and compares different classical-shadow and derandomization strategies rather than using a full exhaustive measurement approach.

<h2 id="methodology" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">🧪 Methodology</h2>

The thesis follows a compact research pipeline that links quantum measurements to classical prediction:

1. Build the molecular / VQE setting for the H2 system and derive Pauli / fermionic operator representations.
2. Generate measurement outcomes using classical-shadow and derandomized measurement strategies, including comparison against randomized baselines.
3. Convert those outcomes into structured datasets of observable and coefficient features.
4. Train classical ML/DL models (for example, regression and tree-based approaches, with LSTM / Bi-LSTM style experimentation in the related workflow) to predict expectation values.
5. Evaluate the effect of measurement budget, optimizer choices, and data preprocessing on prediction quality.

This is the practical core of the project: turning a quantum expectation-value estimation problem into a classical learning problem that can be studied and compared across multiple experiment versions.

<h2 id="project-structure" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">🗂️ Project structure</h2>

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

<h2 id="installation" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">⚙️ Installation</h2>

```bash
git clone https://github.com/your-username/Transformation-of-Quantum-Expectation-value-problem-to-Classical-ML-and-DL-Problem.git
cd Transformation-of-Quantum-Expectation-value-problem-to-Classical-ML-and-DL-Problem
pip install numpy pandas scikit-learn catboost qiskit qiskit-nature jupyter
```

<h2 id="tools" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">🧰 Tools</h2>

**Research stack used in this thesis workflow**

- **Quantum / chemistry:** Qiskit, Qiskit Nature, VQE setup, fermionic-to-qubit mapping.
- **Data / analysis:** Python, Jupyter, NumPy, Pandas, Matplotlib, Plotly.
- **Machine learning:** Scikit-learn, CatBoost, regression and prediction workflows.
- **Interpretability:** LIME, SHAP, ELI5 for model explanation and insight.
- **Development environment:** VS Code for experiment files, notebooks, and repository organization.
- **Hardware context:** NISQ-era research computing with optional GPU/TPU acceleration for heavier ML tasks.

This toolchain connects the quantum and classical parts of the project in one reproducible pipeline.

<h2 id="usage" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">🚀 Usage</h2>

Run the experiment scripts from the relevant folder:

```bash
cd "Classical Machine learning and Deep learning/V13"
python data_acquisition_shadow.py
python prediction_shadow.py
```

You can also open the notebook workflow in the same experiment directory for interactive analysis.

<h2 id="results" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">📈 Results</h2>

The repository is research-oriented rather than a benchmark-style classification project. The main evaluation target is expectation-value prediction quality under different quantum measurement and classical modeling settings.

The thesis emphasizes:
- RMSE / MAE / regression-style comparison for expectation-value prediction
- Comparison between classical-shadow and derandomized measurement strategies
- Comparison among classical ML and DL approaches across the `V13`, `V14`, and `V16` experiment folders, including SMAGON and non-SMAGON variants
- Sensitivity to measurement budget and VQE / optimizer settings, which are central to the project’s experimental discussion

<h2 id="project-flow" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">🔄 Project flow</h2>

```text
H2 / VQE chemistry setup
        ↓
Fermionic → qubit operators
        ↓
Classical-shadow + derandomized measurements
        ↓
Pauli operators + expectation values + coefficients
        ↓
Data cleaning, normalization, train/test split
        ↓
Classical ML / DL regression models
        ↓
Performance comparison + explainability analysis
```

This diagram summarizes the thesis workflow from quantum measurement generation to classical expectation-value prediction and evaluation.
<h2 id="extended-papers-reference-implementations-and-learning-resources" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">📚 Further reading & references</h2>

<h3 style="color:#111827; margin-top:1rem; font-weight:600;">📄 Core research papers</h3>

1. Predicting many properties of a quantum system from very few measurements  
   https://www.nature.com/articles/s41567-020-0932-7

2. Efficient estimation of Pauli observables by derandomization  
   https://arxiv.org/abs/2103.07510

3. Information-theoretic bounds on quantum advantage in machine learning  
   https://arxiv.org/abs/2101.02464

<h3 style="color:#111827; margin-top:1rem; font-weight:600;">💻 Reference implementations</h3>

1. https://github.com/hsinyuan-huang/predicting-quantum-properties
2. https://github.com/renatawong/classical-shadow-vqe

<h3 style="color:#111827; margin-top:1rem; font-weight:600;">🎓 Learning resources</h3>

1. https://www.youtube.com/watch?v=NXejv2wVwas
2. https://www.classiq.io/algorithms/variational-quantum-eigensolver-vqe
3. https://qiskit-community.github.io/qiskit-nature/tutorials/06_qubit_mappers.html
4. https://www.youtube.com/watch?v=YtepXvx5zdI

<h2 id="license" style="color:#111827; border-bottom:2px solid #e5e7eb; padding-bottom:6px; margin-top:2rem;">📜 License</h2>

This repository is intended for academic and research use. Please credit the related quantum-shadow, VQE, and classical ML/DL references in this project when reusing or extending the work.
