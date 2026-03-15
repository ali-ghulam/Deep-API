# Deep-API
Deep-API: Adapter Proteins Identifier using Deep Learning Model with Trisection-Based Evolutionary Features 
# Adaptor Protein Classification Framework Pipeline
This project implements the framework by shared: Dr. Ali Ghulam

1. Data loading from FASTA
2. Optional feature extraction:
   - GAAC
   - PSSM composition
   - CST-PSSM
3. Sequence encoders for deep learning
4. CNN model
5. Bi-LSTM model
6. Ensemble classifier
7. Train/test workflow
8. Evaluation metrics and saved outputs

## Important note
True PSSM and CST-PSSM features require PSI-BLAST-generated ASCII `.pssm` files named as:

## Project structure
- `src/data_utils.py` FASTA parsing, labels, splits
- `src/features.py` GAAC, PSSM, CST-PSSM extraction
- `src/dataset.py` PyTorch dataset classes
- `src/models.py` CNN, Bi-LSTM, ensemble utilities
- `src/train_utils.py` training, validation, testing
- `src/metrics.py` classification metrics
- `src/run_pipeline.py` end-to-end framework runner

## Install
```bash
pip install torch pandas numpy scikit-learn
```

-------------------------------------------------------------

## Outputs
- `outputs/train_features.csv`
- `outputs/test_features.csv`
- `outputs/metrics_cnn.json`
- `outputs/metrics_bilstm.json`
- `outputs/metrics_ensemble.json`
- `outputs/predictions_*.csv`
- saved model checkpoints
