# Beyond Combinations
### Visual Generalization to Unseen Attribute–Object Combinations

## Overview

Beyond Combinations is a Deep Learning project that explores visual classification of familiar and unseen combinations of object attributes, specifically shape and color.

The project uses Convolutional Neural Networks (CNNs) to examine whether models can recognize new combinations of previously encountered visual attributes.

For example, a model may be trained on red cubes, blue cubes, and blue cylinders, then evaluated on a red cylinder that was not present in the training combinations.

## Objectives

- Develop a CNN-based image classification system for object shape and color recognition.
- Compare joint classification and factorized multi-head classification approaches.
- Evaluate model performance on seen and unseen attribute–object combinations.
- Analyze classification errors and differences in generalization performance.

## Dataset

**CLEVR-CoGenT (Condition Generalization Test)**

CLEVR-CoGenT is a synthetic visual dataset containing rendered scenes with objects described by attributes such as shape and color.

The project uses:

- **Condition A:** Training and validation data.
- **Condition B:** Validation samples containing selected unseen cube–color and cylinder–color combinations.

Object attributes and spatial information will be extracted from the corresponding scene JSON annotations.

Dataset source: [CLEVR – Stanford University](https://cs.stanford.edu/people/jcjohns/clevr/)

## Model Architectures

### Model A – Joint Classifier

A CNN that predicts each shape–color combination as a separate class.

### Model B – Factorized Two-Head Classifier

A CNN with a shared feature extraction backbone and two independent classification heads:

- Shape prediction: 3 classes.
- Color prediction: 8 classes.

Both models will use comparable convolutional backbones to support a fair comparison.

## Evaluation

Model performance will be evaluated using:

- Shape Accuracy
- Color Accuracy
- Joint Attribute Accuracy
- Precision, Recall, and F1-score
- Confusion Matrices
- Training and Validation Loss
- Generalization Gap between seen and unseen combinations

## Technologies

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- PIL
- Matplotlib
- Scikit-learn
- Kaggle Notebooks
- Git and GitHub

## Project Structure

```text
Beyond-Combinations/
├── configs/
├── notebooks/
├── src/
├── results/
│   ├── figures/
│   └── metrics/
├── reports/
├── .gitignore
├── README.md
└── requirements.txt
```

## Development Status

<em>Currently in the dataset exploration and preprocessing stage.</em>

Model implementation, training, evaluation, and comparison will follow.

## Author

**Maram Ashraf**

Bachelor of Artificial Intelligence  
Al-Zaytoonah University of Jordan
