# DySCNN: Dynamic S-Box Generation using Convolutional Networks for Efficient Color Image Encryption

Official repository for the paper **"Dynamic S-box Generation using Convolutional Networks for Efficient Color Image Encryption"**.

This repository contains all necessary resources, datasets, pretrained artifacts, and Jupyter notebooks to ensure 100% reproducibility of the experiments, metrics, and generated figures.

---

# Repository Structure

```text
DySCNN/
├── data/
│   └── input_images/          # Standard test images (.png)
├── notebooks/
│   ├── cnn_s-box.ipynb        # Dynamic S-box generation via CNN
│   ├── cifrado.ipynb          # Image encryption/decryption & security tests
│   └── SSIM_PSNR_MAE.ipynb    # Perceptual quality & robustness metrics
└── results/                   # Generated figures (.png, .pdf, .tiff), S-boxes (.npy), and tables (.csv)

 Reproducibility & Execution Guide (Google Colab)
To reproduce the experimental results directly in Google Colab without installing local dependencies, follow these steps:

1. Clone the Repository & Set Up Environment
Run the following commands in a Colab code cell:

!git clone https://github.com/gaussluis/DySCNN.git
%cd DySCNN/notebooks

2. Run Notebooks in Order
Execute the notebooks located in the notebooks/ directory according to your validation objective:

cnn_s-box.ipynb

Trains/loads the CNN model to generate dynamic substitution boxes (S-boxes).

Validates mathematical cryptographic properties (non-linearity, SAC, BIC, strict chaos conditions).

cifrado.ipynb

Performs color image encryption and decryption routines on test images (airplane, baboon, barbara, cameraman, peppers).

Calculates core security metrics: Histogram Analysis, Information Entropy, NPCR, UACI, and Key Sensitivity.

SSIM_PSNR_MAE.ipynb

Evaluates visual degradation, noise resistance (Salt & Pepper, Gaussian), and data loss (clipping attacks).

Computes quantitative image quality metrics: PSNR, SSIM, and MAE.

 Outputs & Results
All execution results are automatically exported to relative paths in the results/ folder:

Numerical Tables: Exported as .csv files (table1_encryption_metrics.csv, table2_robustness_metrics.csv, etc.).

High-Resolution Figures: Saved simultaneously in publication-ready formats (.png, .pdf, .tiff at 300 DPI).

 Citation
If you find this code or research useful in your work, please cite our manuscript:
@article{LopezMaldonado2026DySCNN,
  title={Dynamic S-box Generation using Convolutional Networks for Efficient Color Image Encryption},
  author={Lopez-Maldonado, Jose Luis and collaborators},
  journal={Journal Name},
  year={2026}
}

