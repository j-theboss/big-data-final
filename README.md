# Deep Learning with Keras API - Project README

## Overview

This project focuses on deep learning using the Keras API within TensorFlow. The notebook demonstrates how to build, train, and evaluate neural networks for machine learning tasks. Below, you'll find details about the key sections and steps presented in the notebook.

## Requirements

To replicate the results or run the code from the notebook, install the following dependencies:

- Python 3.x
- TensorFlow (>= 2.x)
- Keras
- NumPy
- Matplotlib
- Jupyter Notebook (optional, for running the `.ipynb` file)

Install the dependencies using:

```bash
pip install tensorflow numpy matplotlib jupyter
```

## Key Features

- **Model Construction:** Demonstrates how to build a sequential model using Keras layers.
- **Data Preprocessing:** Provides insights into data loading, normalization, and preparation.
- **Model Compilation:** Shows how to configure the loss function, optimizer, and evaluation metrics.
- **Model Training:** Utilizes `model.fit()` for training with batch processing.
- **Evaluation:** Evaluates model performance and visualizes learning curves.
- **Visualization:** Includes plots of model loss and accuracy metrics over training epochs.

## Usage

1. **Clone the Repository:**

   ```bash
   git clone <repo-url>
   cd <repo-folder>
   ```

2. **Launch Jupyter Notebook:**

   ```bash
   jupyter notebook Copia_de_dllib_keras_api.ipynb
   ```

3. **Run the Cells:** Execute each code cell in sequence for a step-by-step guide on using the Keras API.

## Example Commands

Below are examples of core operations covered in the notebook:

### Define the Model

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense

model = Sequential([
    Dense(32, activation='relu', input_shape=(input_dim,)),
    Dense(16, activation='relu'),
    Dense(1, activation='sigmoid')
])
```

### Compile the Model

```python
model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
```

### Train the Model

```python
history = model.fit(X_train, y_train, epochs=20, batch_size=32, validation_data=(X_val, y_val))
```

### Plot Training History

```python
import matplotlib.pyplot as plt
plt.plot(history.history['loss'], label='train loss')
plt.plot(history.history['val_loss'], label='val loss')
plt.legend()
plt.show()
```

## Results

- The notebook showcases model training and validation processes.
- Learning curves (loss and accuracy) help visualize model performance over time.

## Notes

- Modify hyperparameters like the number of epochs, batch size, and learning rates for experimentation.
- Ensure proper dataset preprocessing for optimal model performance.

## Conclusion

This project serves as a comprehensive introduction to deep learning with Keras, guiding users through essential steps from model creation to evaluation.

