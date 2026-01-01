# Sensitivity Analysis of Image Classification Models using Generalized Polynomial Chaos

This repository contains the code for the research paper titled "Sensitivity Analysis of Image Classification Models using Generalized Polynomial Chaos", which is currently published as a preprint on arXiv. Here, we provide all the necessary information and resources to reproduce the results presented in our paper.

## Abstract

Integrating advanced communication protocols in production has accelerated the adoption of data-driven predictive quality methods, notably machine learning (ML) models. However, ML models in image classification often face significant uncertainties arising from model, data, and domain shifts. These uncertainties lead to overconfidence in the classification model's output. To better understand these models, sensitivity analysis can help to analyze the relative influence of input parameters on the output. This work investigates the sensitivity of image classification models used for predictive quality. We propose modeling the distributional domain shifts of inputs with random variables and quantifying their impact on the model's outputs using Sobol indices computed via generalized polynomial chaos (GPC). This approach is validated through a case study involving a welding defect classification problem, utilizing a fine-tuned ResNet18 model and an emblem classification model used in BMW Group production facilities.

## Citation

If you find this work useful for your research, please cite our paper:

```bibtex
@article{bahr2024sensitivity,
  title={Sensitivity Analysis of Image Classification Models using Generalized Polynomial Chaos},
  author={Bahr, Lukas and Possner, Lucas and Weise, Konstantin and Gröger, Sophie and Daub, Rüdiger},
  journal={arXiv preprint arXiv:2506.18751},
  year={2025}
}
```

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/lpossner/gPC_Image_Classification.git
cd gPC_Image_Classification
```

### 2. Install Dependencies

```bash
pip install uv
uv sync
```

### 3. Download Dataset
Download the [TIG Aluminium 5083 dataset](https://www.kaggle.com/datasets/danielbacioiu/tig-aluminium-5083/) from Kaggle and place it in the `data/` directory.

## Usage

The workflow consists of three main steps:

### 1. Fine-tune the Model
Train the ResNet18 model on the welding defect classification task:
```bash
python fine_tune_model.py
```

### 2. Prepare Data for Sensitivity Analysis
Generate augmented datasets with distributional shifts:
```bash
python create_data.py
```

### 3. Run gPC Sensitivity Analysis
Compute Sobol indices to quantify input parameter influence:
```bash
python run_gpc.py
```

## Additional Resources

- [Preprint](https://arxiv.org/abs/2506.18751)
- [Dataset](https://www.kaggle.com/datasets/danielbacioiu/tig-aluminium-5083/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact Information

For any queries regarding the paper or the code, please open an issue on this repository or contact the authors directly at:

- [Lukas Bahr](mailto:lukas.bahr@bmw.de)
