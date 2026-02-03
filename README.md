# Comparing_Weight_Decoded_Tokens_and_Maximally_Activating_Inputs

This repository contains the code, data, and supplementary materials for my thesis on neuron-level interpretability in Transformer feed-forward networks (FFNs).  
The thesis presents a systematic comparison between activation-based and weight-geometry-based methods for analyzing neuron–token selectivity across models of different depths.

---

## 📄 Thesis Overview

Understanding the functional roles of FFN neurons in Transformer models remains a central challenge in mechanistic interpretability.  
This work compares two widely used interpretability perspectives:

- **Method 1: Activation-Based Analysis**  
  Interprets neurons by examining the tokens or contexts that elicit the strongest activations during inference.

- **Method 2: Weight-Geometry (Input-Side) Analysis**  
  Interprets neurons by analyzing the geometric alignment between neuron input weight vectors and token embeddings, providing an input-agnostic view of neuron selectivity.

The comparison is conducted on:
- **Shallow SoLU-based models** (SoLU-1L, SoLU-2L) under controlled settings
- **The deeper `gpt2-small` model** as a realistic case study

The analysis focuses on neuron-level agreement, token-category distributions, and how alignment patterns vary across layers and neuron types.

---

## 🧠 Key Research Questions

- To what extent do activation-based and weight-geometry methods agree on neuron–token selectivity?
- How does this agreement vary across neurons, layers, and model depth?
- What are the strengths and limitations of token-level interpretability when relying on a single method?

---

## 📂 Repository Structure

```text
.
├── thesis/
│   ├── thesis.pdf              # Final thesis document
│   ├── figures/                # Figures used in the thesis
│   └── tables/                 # Tables and supplementary results
│
├── code/
│   ├── method1_activation/     # Activation-based analysis scripts
│   ├── method2_geometry/       # Weight-geometry analysis scripts
│   ├── token_categorization/   # Token category mapping utilities
│   └── utils/                  # Shared helper functions
│
├── data/
│   ├── raw/                    # Raw text or token data
│   └── processed/              # Processed analysis outputs
│
├── results/
│   ├── neuron_cases/           # Neuron-level case studies
│   └── aggregate_stats/        # Aggregate agreement statistics
│
└── README.md
