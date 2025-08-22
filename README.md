# 🌿 Plant Disease Detection and Classification: Baseline Models

This repository contains Google Colab notebooks for baseline deep learning models used in plant disease classification with the publicly available [PlantVillage dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset).


## Models Included 

| Model         | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| **CNN**       | A standard convolutional neural network built using TensorFlow. |
| **ViT**       | Vision Transformer using a pre-trained model from [TensorFlow Hub](https://tfhub.dev/sayakpaul/vit_b16_fe/1)            |
| **ViT+CNN**   | A hybrid architecture combining CNN and ViT features before classification.  |

Each model was evaluated using accuracy metrics and GRAD-CAM heatmaps for explainability.

---

## Dataset

- **Name:** PlantVillage
- **Source:** [Kaggle – PlantVillage Dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset)
- **Classes:** 38 categories of healthy and diseased plants
- **Preprocessing:** Images resized to 224×224, normalized, and split into training, validation, and test sets.

---

## Explainability with GRAD-CAM

Each notebook includes **GRAD-CAM visualizations** that highlight the regions in the input leaf images most influential in the model’s predictions. This provides interpretability and helps validate model performance.

> ⚠️ Outputs such as training plots and GRAD-CAM heatmaps are pre-generated and visible in the notebook. Re-running may produce slightly different results due to randomness in training and data processing.

---

## Notes
- The models implemented here (CNN, ViT, and ViT+CNN) are based on standard, well-known architectures implemented as part of my learning journey.
- The repository provides baseline models and explainability tools to serve as reference points for evaluating more advanced plant disease detection models.

---

## Author
[Srijani Das](https://github.com/Srijani-Das07)

---

## License
This repository is released under the [MIT License](LICENSE).

---
