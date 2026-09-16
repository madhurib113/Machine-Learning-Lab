# Experiment 9 – Perceptron vs Multilayer Perceptron

## Aim

To compare a Single-Layer Perceptron (PLA) and a Multilayer Perceptron (MLP) for handwritten English character classification.

## Dataset

Chars74K English Handwritten Characters dataset (EnglishHnd.tgz).

- 3410 handwritten character images
- 62 classes
- Classes include numbers, uppercase letters and lowercase letters

## Models Used

- Perceptron Learning Algorithm (PLA)
- Multilayer Perceptron (MLP)

## Work Done

- Loaded and extracted the EnglishHnd dataset
- Checked the number of classes and images
- Resized the images
- Converted the images into suitable input format
- Normalized the pixel values
- Flattened the images into 784 features
- Split the data into training, validation and test sets
- Implemented PLA
- Implemented MLP using TensorFlow and Keras
- Compared different cost functions
- Tuned hidden layers, activation functions, optimizers, learning rates and batch sizes
- Selected the best MLP configuration based on validation accuracy
- Compared PLA and MLP using accuracy, precision, recall and F1-score
- Generated confusion matrices
- Generated ROC curves
- Plotted training and validation loss

## Hyperparameter Tuning

Different MLP configurations were tested using:

- ReLU and Tanh activation functions
- SGD and Adam optimizers
- Different learning rates
- Different batch sizes
- Different hidden layer sizes

The selected configuration was:

- Hidden layers: 128
- Activation: Tanh
- Optimizer: Adam
- Learning rate: 0.001
- Batch size: 32

The best validation accuracy obtained during tuning was 0.1557.

## Results

### PLA

- Accuracy: 0.1422
- Precision: 0.2574
- Recall: 0.1422
- F1-score: 0.1307

### Tuned MLP

- Accuracy: 0.2331
- Precision: 0.2423
- Recall: 0.2331
- F1-score: 0.2074

## Comparison

| Model | Accuracy | Precision | Recall | F1-score |
|-------|----------|-----------|--------|----------|
| PLA | 0.1422 | 0.2574 | 0.1422 | 0.1307 |
| MLP | 0.2331 | 0.2423 | 0.2331 | 0.2074 |

## Files

- `ML_09.ipynb` – Jupyter Notebook containing the implementation
- `ML_09.pdf` – Report containing the experiment details and results

## Dependencies

The following Python libraries are required to run the notebook:

```text
numpy
pandas
matplotlib
Pillow
scikit-learn
tensorflow
