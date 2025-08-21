# DKD-KAN: Lightweight Intrusion Detection with Kolmogorov–Arnold Networks and Decoupled Knowledge Distillation

This repository contains the official implementation of our lightweight intrusion detection framework introduced in the paper:

> **"Lightweight Intrusion Detection Using Kolmogorov–Arnold Networks and Decoupled Knowledge Distillation"**

## 🚀 Overview

Cyber-security systems often operate in environments with limited resources, such as edge devices and real-time monitoring systems, where **model size** and **inference speed** are critical. To address these challenges, we propose a novel intrusion detection approach that combines:

- **Kolmogorov–Arnold Networks (KAN)**: A high-capacity teacher model that effectively captures complex patterns in attack data.
- **Decoupled Knowledge Distillation (DKD)**: An efficient training strategy to transfer knowledge from the teacher to a lightweight student model.
- **Multi-Layer Perceptron (MLP) Student**: A highly compact model with as few as **2,522 parameters (WADI)** and **1,622 parameters (SWaT)**, designed for deployment in constrained environments.

Despite their small size, our DKD-MLP models achieve strong performance, improving **F1-scores by 4.18% (SWaT)** and **3.07% (WADI)** over standard baselines.

## 📂 Repository Contents

- `swat-dkd.ipynb` – DKD training and evaluation on the SWaT dataset  
- `wadi-dkd.ipynb` – DKD training and evaluation on the WADI dataset  
- `requirements.txt` – Python environment dependencies  
- `README.md` – Project documentation

## 📊 Datasets

We evaluate our method on two publicly available industrial control system datasets:

- [SWaT (Secure Water Treatment)](https://itrust.sutd.edu.sg/itrust-labs_datasets/dataset_info/)
- [WADI (Water Distribution)](https://itrust.sutd.edu.sg/itrust-labs_datasets/dataset_info/)

## 🔧 Requirements

To install the necessary dependencies, run:

```bash
pip install -r requirements.txt
```
## 📊 Datasets

We evaluate our method on two publicly available industrial control system datasets:

- **WADI (Water Distribution)** dataset can be accessed on Kaggle:  
  [https://www.kaggle.com/datasets/giovannimonco/wadi-data](https://www.kaggle.com/datasets/giovannimonco/wadi-data)

- **SWaT (Secure Water Treatment)** dataset can be downloaded using `gdown`:  

  ```bash
  # Install gdown if not already installed
  !pip install gdown
  
  # Download SWaT dataset files
  !gdown 1Q20VOHE0wvl5ASMF_EKo0xM7H6t5YCCf  # Attack_v0
  !gdown 1B42LXq4OXpmjtwFIPw-cSHr6SZzYJDkL  # Normal_v1
  ```

## 🧠 Citation
If you find this work useful, please cite the following article:

```bibtex
@article{alikhani2025contrastive,
  title={Contrastive-KAN: A Semi-Supervised Intrusion Detection Framework for Cybersecurity with scarce Labeled Data},
  author={Alikhani, Mohammad and Kazemi, Reza},
  journal={arXiv preprint arXiv:2507.10808},
  year={2025}
}
@article{alikhani2025kan,
  title={KAN-HAR: A Human activity recognition based on Kolmogorov-Arnold Network},
  author={Alikhani, Mohammad},
  journal={arXiv preprint arXiv:2508.11186},
  year={2025}
}
```
