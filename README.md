# Master thesis repository 2021-2024

Student: Skalvis Paliulis, skalvis.paliulis@gmail.com

Supervisor: Assoc. Prof. Linas Petkevičius (Vilnius University)

Modelling and data analysis master thesis: 

**"INVESTIGATION OF CLASSIFICATION ALGORITHMS IN QUANTUM COMPUTING"**

This repository contains two Jupyter notebook files:
1. Classical algo.ipynb - contains classical classification algorithms' used for benchmark, created using [Pycaret package](https://pycaret.gitbook.io/docs/) Date accessed on 2024-01-06. 
2. Qsvm_marginlos.ipynb - contains variational quantum suport vector machine model and its results. 
	- Initial model structure is build based on PennyLane tutorial by Safwan Hossein. [Multiclass margin classifier](https://pennylane.ai/qml/demos/tutorial_multiclass_classification/) Date accessed: 2023-11-20.

## Data sets
- Fisher's *Iris* data set. Taken from scikit-learn machine learning library.
- Wine Quality data set. Taken from UCI Machine learning repository (ML repo).
- MNIST data set. Taken from UCI Machine learning repository (ML repo).
- Circle data set. Manually generated data set, code for data generation taken from PennyLane tutorial by Shahnawaz Ahmed. [Data-reuploading classifier](https://pennylane.ai/qml/demos/tutorial_data_reuploading_classifier/) Date accessed: 2023-12-27.

## Thesis Aim: 
Empirically investigate classification algorithms in quantum computing using PennyLane framework. Focus to be directed towards already available quantum classification algorithms, 
compared against well-established classical algorithms. Moreover, we ought to cover supervised learning algorithms. In terms of classification task, single-class/binary and multi-class classification
algorithm benchmarks assessed using standard metrics. Throughout experiment, mostly locally held simulators to be used. 

## Thesis Objectives:
1. Carry out the scientific literature review of classification algorithms which are implementable in quantum computing.
2. Identify the algorithms for further analysis.
3. Identify and select data sets for bench-marking and classification algorithms.
4. Investigate and compare the selected algorithms on benchmarks setup using quantum simulators (or quantum computer).
5. Provide the results, insights and recommendations on using quantum classification algorithms in practice.

## Data Preparation
- **Iris, Wine Quality and Circle** data sets had similar data preparation stages:
	1. All feature value vectors were divided by their L2 norms.
	2. All respective classes were converted to natural numbers $\mathbb{N} = [0, 1, 2, \ldots, N-1.]$.
	3. Wine Quality data set specifically, had reduced overall sample size fed to pipeline. From 6497 -> 1000 observations.
	4. Data sets were split into train:test sets, by 0.75 : 0.25, respectively.
- **MNIST**, due to high  dimensional data, additional steps were introduced:
	1. Sample size reduced from 70,000 -> 1000 observations.
	2. Data dimension reduced from 784 columns (28x28) to 2, using combination of [SVD](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.TruncatedSVD.html) and [t-SNE](https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html).
		- Preprocessing example taken from [Qiskit Challenge India 2020](https://github.com/Qiskit-Challenge-India/2020/blob/master/Day%206%2C%207%2C8/VQC_notebook.ipynb). 

## Experiment Setup
**PyTorch interface for PennyLane framework, with default.qubit simulator, to implement multiple one-vs-all classifiers.**

### Environment and Carcass
Experiment was carried in Python 3 programming language using Jupyter Notebooks. Codes themselves were ran on [Google Colab](https://colab.research.google.com/) environment, Linux based VM with integrated Python 3 environment. 
CPU consisted of two Intel(R) Xeon(R) CPU @ 2.20GHz processors.

### Quantum Processing Unit Part
1. Amplitude Embedding used for state preparation $S_{x}$.
2. Using unitary gate operations ($U_{\theta}$), qubit computational basis states are processed.
3. Class predictions $p(y)$ and score $s$ received during measurement. 

Computational scheme Ansatz example for Iris data set:
![Iris QSVM Ansatz](/Quantum-2024/Images_and_results/QSVM_iris_schema_corrected.png?raw=true "Iris Ansatz")

### Classical Processing Unit Part
1. Optimization done using Adam - Adaptive Moment estimation algorithm.
2. Loss function - Margin Loss : $L(x,y) = \sum_{j\neq y}\max(0,s_{j}-s_{y}+\Delta)$.

## Results
1. Applied Quantum Support Vector variational classifier and applied to 4 heterogeneous data sets, creating 4 separate 2-qubit, 4-qubit and two 1-qubit systems/ansatz.
2. QSVM with 219 learnable parameters and 12 features took 424.139 (s) less time to train than QSVM model with 57 parameters and 2 features. TT 1199.929 (s) and 1624.068 (s), respectively.
3. Best QSVM performance was noticed for Iris data set (Accuracy: 0.9737, Recall : 0.9762, Precision : 0.9744 and F1Score : 0.9743), same quantum model outperformed also 14 out of 15 classical algorithms for given data set.
4. Worst QSVM performance was noticed for MNIST data set, which was outperformed by 12 out of 15 classical algorithms and QSVM for Wine Quality data set which was outperformed by 14 out of 15 classical algorithms.
5. QSVM for non-linear Circle data set returned similar results comparing with classical algorithms.

From the results we could draw such conclusions:

1. In general classical models outperform QSVM model with margin loss.
2. No one classical algorithm outperforms other classical counterparts on all data sets.
3. Running model on near-term quantum device could improve model performance.
4. Increasing iteration count for training procedure might improve overall QSVM accuracy.

Further result tables can be found [here](https://github.com/Skalvis/Quantum-2024/Images_and_results/results.md) 

# Dislaimer
All credits to their original authors from PennyLane for code reused in this work, as well as, for data preprocessing from Qiskit Challenge India 2020 for t-SNE and SVD application for high dimensional data. 

# Key References
- Shahnawaz Ahmed. Data-reuploading classifier. (https://pennylane.ai/qml/demos/tutorial_data_reuploading_classifier/), 09 2019. Date Accessed: 2023-12-27.
- Ville Bergholm *et al*, Pennylane: Automatic differentiation of hybrid quantum-classical computations, 2022.
- M. Cerezo *et al*,  Variational quantum algorithms. Nature Reviews Physics, 3(9):625–644, August 2021.
- Safwan Hossein. Multiclass margin classifier. (https://pennylane.ai/qml/demos/tutorial_multiclass_classification/), 03 2020. Date Accessed: 2023-11-20.
- Adrián Pérez-Salinas, Alba Cervera-Lierta, Elies Gil-Fuster, and José I. Latorre. Data re-uploading for a universal quantum classifier. Quantum, 4:226, February 2020.
- Maria Schuld. Supervised quantum machine learning models are kernel methods, 2021.
- Maria Schuld, Alex Bocharov, Krysta M. Svore, and Nathan Wiebe. Circuit-centric quantum classifiers. Physical Review A, 101(3), March 2020.
- Maria Schuld and Francesco Petruccione. Machine Learning with Quantum Computers. Springer Cham, Cham, Switzerland, 2021. 312 p.
- K. Mitarai, M. Negoro, M. Kitagawa, and K. Fujii. Quantum circuit learning. Physical Review A, 98(3), September 2018.
