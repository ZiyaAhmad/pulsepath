# PulsePath
ML-program built for the Synopsys Science Fair 2025-26.

Presentation trifold can be found here: [https://docs.google.com/presentation/d/1ubiWkkjD9npzASVNndkHZ8OacZJq7ahLl7JQLaWFG90/edit?usp=sharing](https://docs.google.com/presentation/d/1ubiWkkjD9npzASVNndkHZ8OacZJq7ahLl7JQLaWFG90/edit?usp=sharing)

## Repository Structure
| File | Description |
|---|---|
| `downloading_ecg.ipynb` | Downloads the MIT-BIH SVDB dataset from PhysioNet and segments it into labeled 12-second windows |
| `train_test_split.ipynb` | Creates and saves a stratified train/test split from the processed dataset |
| `model1_normal_vs_abnormal.ipynb` | Trains Model 1 (normal vs. abnormal) |
| `model2_sva_vs_presva.ipynb` | Trains Model 2 (SVA vs. pre-SVA) |
| `chain_model.ipynb` | Evaluates the full chain model pipeline and generates the confusion matrix |

## Running the Notebooks
These notebooks are designed to run on **Google Colaboratory** with a GPU runtime (we used an A100). To get started:

1. Run `downloading_ecg.ipynb` to generate `ecg_data.npz`
2. Run `train_test_split.ipynb` to generate `train_test_split.npz`
3. Train both models using `model1_normal_vs_abnormal.ipynb` and `model2_sva_vs_presva.ipynb`
4. Evaluate the full pipeline with `chain_model.ipynb`
