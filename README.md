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
Install dependencies:

pip install tensorflow biopython scikit-learn imageio matplotlib


Run the Colab notebook:

Download datasets: CullPDB5926-filtered and CB513.

Preprocess sequences and labels.

Train the CNN+BiLSTM model.

Evaluate and visualize results (plots, confusion matrices, weight GIFs).

Outputs

figures/ – loss/accuracy curves, confusion matrix, model diagram.

gifs/ – weight-update GIFs per layer.

best_model.keras – best-trained Keras model.

training_history.json – per-epoch metrics for tracking training progress.

Usage Notes

Set FAST_DEMO=True for quick testing on a subset of data.

Full training may take several hours depending on GPU availability.

Sample weights are used during training to ignore padded positions in sequences.

Evaluation

Produces a Q8 classification report with precision, recall, and F1-score.

Confusion matrix visualizations for Q8 classes: L, B, E, G, I, H, S, T.

Optional mapping to Q3 classes (H, E, C) for simplified secondary structure analysis.

License

This project is for educational purposes only. Use responsibly and cite appropriately.


This version is **complete, self-contained, and ready for GitHub**.  

If you want, I can also make an **even shorter version with bullets only for quick reading** whi
