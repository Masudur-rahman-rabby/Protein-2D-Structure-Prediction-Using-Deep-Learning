# Protein-2D-Structure-Prediction-Using-Deep-Learning
# Protein 2D Structure Prediction Using Deep Learning

## Overview
This project predicts protein secondary structures (Q8) directly from amino acid sequences using a deep learning model that combines Convolutional Neural Networks (CNN) and Bidirectional LSTM (BiLSTM). It captures both local and long-range dependencies in protein sequences for accurate per-residue classification.

## Features
- Collects diverse protein sequences from **NCBI** (FASTA format).
- Uses **CullPDB5926-filtered** for training/validation and **CB513** for testing.
- Preprocesses sequences with one-hot encoding and optional PSSM profiles.
- Handles variable-length sequences with padding and masking.
- Trains a deep learning model with masked categorical cross-entropy to ignore padded residues.
- Evaluates performance using accuracy, precision, recall, F1-score, and confusion matrices.
- Visualizes training curves and weight updates with GIFs and plots.

## Getting Started
1. **Clone the repository**:
   ```bash
   git clone <your-repo-url>
   cd <repo-folder>
