# Protein 2D Structure Prediction Using Deep Learning

## Overview
This project predicts protein secondary structures (Q8) directly from amino acid sequences using a deep learning model combining Convolutional Neural Networks (CNN) and Bidirectional LSTM (BiLSTM). It captures both local and long-range dependencies for accurate per-residue classification.

## Methodology
1. **Data Collection**:  
   - Diverse protein sequences collected from **NCBI** (FASTA format).  
   - Labeled benchmark datasets: **CullPDB5926-filtered** for training/validation and **CB513** for testing.

2. **Preprocessing**:  
   - One-hot encoding for amino acids.  
   - Optional PSSM profiles for enhanced feature representation.  
   - Variable-length sequences padded/truncated to 700 residues.  
   - Masking applied to ignore padded residues during training.

3. **Model Architecture**:  
   - **Input**: Sequence features (one-hot + optional PSSM).  
   - **Layers**: Conv1D → BatchNorm → Dropout → BiLSTM → Conv1D → Dropout → TimeDistributed Dense → Softmax.  
   - **Output**: Q8 classification per residue.  
   - Model diagram saved as `figures/model.png`.

4. **Training**:  
   - Masked categorical cross-entropy loss.  
   - Sample weights applied to ignore padded positions.  
   - Callbacks: EarlyStopping, ReduceLROnPlateau, ModelCheckpoint, and Weight GIF visualizer.

## Results
- **Evaluation Metrics**: Accuracy, precision, recall, F1-score for Q8 classes (`L, B, E, G, I, H, S, T`).  
- **Visualizations**:  
  - Loss & accuracy curves (`figures/loss_curve.png`, `figures/accuracy_curve.png`).  
  - Confusion matrix (`figures/confusion_matrix.png`).  
  - Weight-update GIFs per layer (`gifs/`).  
- Optional Q8 → Q3 mapping for H/E/C secondary structure analysis.

## Outputs
- `figures/` – loss/accuracy curves, confusion matrix, model diagram.  
- `gifs/` – weight-update GIFs per layer.  
- `best_model.keras` – best-trained Keras model.  
- `training_history.json` – per-epoch training metrics.  

## Conclusion
This deep learning approach efficiently predicts protein secondary structures using sequence features and optional PSSM profiles. The CNN+BiLSTM model captures both local patterns and long-range dependencies, achieving robust performance on CB513 test data. Future improvements can include attention mechanisms or transformer-based models for enhanced accuracy.

## License
Educational use only. Cite appropriately if used in research or projects.
