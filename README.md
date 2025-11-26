# R3D-demo

This repository contains a demonstration and visualization resources for **R3D**, a depth-informed fusion framework introduced in the paper **"Countering Multi-modal Representation Collapse through Rank-targeted Fusion" (WACV 2026)**.

## 📝 Overview

**R3D** proposes a **Rank-enhancing Token Fuser (RTF)** to address feature collapse and modality collapse in multi-modal learning. The method selectively blends features from one modality with complementary features from another to increase the effective rank of the fused representation, thereby enhancing the information content and improving performance in Action Anticipation tasks.

This demo specifically highlights:
* **Feature Visualization**: Visualizing raw depth features vs. "exchanged" or fused features.
* **Rank Analysis**: Demonstrating the effective rank gain achieved through the fusion process.
* **DARai Dataset**: Utilizing samples from the *Daily Activity Recordings for artificial intelligence* (DARai) dataset.

## 📂 Repository Structure

* **`r3d_demo.ipynb`**: The main Jupyter Notebook containing the code to load features, compute effective rank, and visualize the results.
* **`rgb/`**: Contains sample RGB frames from the dataset (e.g., `01_3_00072.jpg`, `01_3_00599.jpg`).
* **`pt_darai_depth/`**: Directory containing PyTorch tensors (`.pt`) representing feature embeddings:
    * **`depth_raw/`**: Raw depth feature tokens before fusion.
    * **`rgb_raw/`**: Raw RGB feature tokens before fusion.
    * **`exchanged_depth/`**: Depth features after the token exchange/fusion process.
    * **`exchanged_rgb/`**: RGB features after the token exchange/fusion process.
    * **`effective_rank_gain_plot.png`**: Generated plot illustrating the increase in effective rank.

## 🚀 Getting Started

### Prerequisites
To run the demo notebook, you will need the following Python libraries:
* `torch`
* `numpy`
* `matplotlib`
* `Pillow`

### Running the Demo
1.  Clone this repository.
2.  Ensure you have the sample data (the `pt_darai_depth` and `rgb` folders) in the root directory.
3.  Open `r3d_demo.ipynb` in Jupyter or Google Colab.
4.  Run the cells to visualize the original vs. exchanged features and analyze the rank enhancement.

## 📄 Citation

If you use this code or the R3D framework in your research, please cite the original paper:

> **Countering Multi-modal Representation Collapse through Rank-targeted Fusion**
> *Seulgi Kim, Kiran Kokilepersaud, Mohit Prabhushankar, Ghassan AlRegib*
> arXiv preprint arXiv:2511.06450 (2025)

## 🔗 Related Resources

* **Main Repository**: [https://github.com/olivesgatech/R3D](https://github.com/olivesgatech/R3D)
* **DARai Dataset**: [https://github.com/olivesgatech/DARai](https://github.com/olivesgatech/DARai)
* **OLIVES Lab**: [https://alregib.ece.gatech.edu/](https://alregib.ece.gatech.edu/)
