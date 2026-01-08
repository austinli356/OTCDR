# OTCDR

OTCDR: Optimal Transport–Guided Cancer Drug Response Prediction
Overview

<img width="1173" height="703" alt="Diagram" src="https://github.com/user-attachments/assets/471f1561-7765-47ff-acb0-95d48f26bca3" />

OTCDR is a matrix factorization–based framework for predicting interactions between anticancer drugs and cancer cell lines. The model integrates graph-based molecular representations, optimal transport–derived similarity measures, and ridge regression–regularized matrix factorization to produce biologically meaningful and generalizable predictions of drug response.

This repository contains the full computational pipeline supporting the OTCDR model, including data preprocessing, similarity computation, network integration, model training, and evaluation under cross-validation. The code is designed to support reproducible research while showcasing modern machine learning and scientific computing techniques applicable to real-world biomedical problems.

Methodological Summary

OTCDR is motivated by the observation that effective drug response prediction requires capturing both:

Topological structure of molecular graphs, and

Distributional relationships across drug–cell line interaction profiles.

To this end, the framework consists of the following core components:

Graph-Based Drug Representations
Drugs are represented as graphs derived from molecular structure, enabling the model to encode chemically meaningful topology rather than relying solely on hand-crafted descriptors.

Optimal Transport–Based Similarity Computation
Optimal transport is used to compute similarity matrices that capture distributional alignment between drugs and/or cell lines. This allows the model to compare entities in a way that is robust to structural variability while preserving global relational information.

Integrated Interaction Network Construction
Similarity matrices and known drug–cell line interactions are combined into a unified network representation, serving as the foundation for downstream learning.

Matrix Factorization with Ridge Regression
The integrated network is factorized using matrix factorization, with ridge regression providing regularization to control overfitting and improve generalization. The resulting latent representations are used to reconstruct a rating matrix from which interaction predictions are derived.

Model Performance

OTCDR is evaluated using 5-fold cross-validation and demonstrates strong predictive performance relative to existing methods:

![Figure A_page-0001](https://github.com/user-attachments/assets/10b75db3-d172-44a5-8092-25e4caefced5)

These results indicate robust generalization and strong ranking performance in a challenging, imbalanced prediction setting.
