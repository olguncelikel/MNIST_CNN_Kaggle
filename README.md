# MNIST CNN Kaggle

This project contains a Convolutional Neural Network (CNN) for classifying handwritten digits from the Kaggle MNIST dataset.

The notebook in this repository loads the training and test data, preprocesses the pixel values, builds a deep learning model, trains it, and generates predictions for submission.

## Project overview

- Dataset: Kaggle MNIST handwritten digit dataset
- Task: Multi-class image classification (digits 0-9)
- Model: CNN built with TensorFlow/Keras
- Goal: Achieve high accuracy on digit recognition

## Repository contents

- `MNIST_CNN_Kaggle.ipynb` — main notebook with data loading, preprocessing, model training, and predictions
- `train.csv.zip` — zipped training data
- `test.csv.zip` — zipped test data
- `README.md` — project documentation

## Requirements

Make sure you have the following installed:

- Python 3.10+
- Jupyter Notebook or JupyterLab
- TensorFlow
- NumPy
- Pandas
- Matplotlib
- scikit-learn (optional, for evaluation utilities)

You can install the dependencies with:

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn
```

## Data

The dataset files are provided as CSV archives in the repository root:

- `train.csv.zip`
- `test.csv.zip`

These contain the pixel matrix for each handwritten digit image. A typical MNIST image is a 28x28 grayscale image, flattened into a vector of length 784 for each sample.

## Workflow

1. Extract the ZIP files if needed.
2. Load the train and test CSV files.
3. Normalize pixel values to the range [0, 1].
4. Reshape the data into 28x28x1 arrays.
5. Build a CNN model.
6. Train the model on the training set.
7. Evaluate performance.
8. Generate predictions for the test set.

## Model architecture

The notebook typically uses a CNN with layers such as:

- Input layer (28x28x1)
- Convolutional layer(s)
- ReLU activation
- Max pooling layers
- Flatten layer
- Dense (fully connected) layers
- Softmax output layer for 10 classes

## Running the notebook

Open the notebook in Jupyter and run all cells:

```bash
jupyter notebook MNIST_CNN_Kaggle.ipynb
```

Or use JupyterLab:

```bash
jupyter lab
```

## Output

After training, the notebook produces:

- Model accuracy/loss metrics
- Predicted labels for the test set
- Submission-ready output file if configured

## Notes

- MNIST is a classic benchmark dataset used for image recognition tasks.
- Because the data is grayscale and already normalized in typical Kaggle competitions, preprocessing is usually straightforward.
- If you want to improve performance, you can experiment with:
  - more convolutional layers
  - dropout
  - data augmentation
  - learning rate scheduling
  - transfer learning

## License

This repository is provided for educational and experimentation purposes. Please check the Kaggle competition rules or dataset usage terms if you plan to submit results publicly.

## Author

Created for a CNN-based MNIST classification project using Kaggle data.
