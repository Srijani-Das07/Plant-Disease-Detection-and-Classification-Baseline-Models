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

###  Model Details

#### 1. Convolutional Neural Network (CNN)

**Overview**  
A CNN is designed to capture **local patterns** in images, such as edges, textures, and disease spots on leaves.  

**Architecture Used**  
- Multiple convolutional and pooling layers for hierarchical feature extraction.  
- Flatten layer followed by fully connected (dense) layers.  
- Softmax output layer for classification into 38 classes.  

**Strengths**  
- Excellent at identifying fine-grained disease symptoms (e.g., small brown spots, color changes).  

**Limitations**  
- Focuses on local features and may miss **global context** (overall leaf shape or spatial relationships).  

---

#### 2. Vision Transformer (ViT)

**Overview**  
ViT treats an image as a **sequence of patches**, similar to how words are treated in NLP (Natural Language Processing) tasks. It uses **self-attention** to learn global dependencies across the entire image.   

**Strengths**  
- Captures long-range relationships and overall structure of the leaf.  
- Benefits from transfer learning with large-scale pre-training.  

**Limitations**  
- Requires more computational resources.  
- Not as specialized in capturing **low-level local textures** as CNNs.  
---

#### 3. Hybrid CNN + ViT

**Overview**  
This model combines **CNN’s local feature extraction** with **ViT’s global attention** to leverage both perspectives.  

**Architecture**  
- A **CNN branch** processes the input image to extract low-level texture and edge features.  
- A **ViT branch** processes the same image as patches for capturing global context.  
- The outputs from both branches are **concatenated** and passed to dense layers for classification.  

**Strengths**  
- Achieves **balanced performance** by integrating both local and global representations.  
- More robust in detecting complex disease patterns that span across different regions of the leaf.  

**Use Case**  
Serves as a strong **baseline hybrid architecture** for further experimentation.

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
- *Detailed training results and evaluation metrics for each model are available directly inside the notebooks.*

---

## Author
[Srijani Das](https://github.com/Srijani-Das07)

---

## License
This repository is released under the [MIT License](LICENSE).

---
