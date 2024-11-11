## Hyperparameter Tuning

Hyperparameter tuning is a crucial step in optimizing machine learning models. In this project, I use Grid Search to identify the best combination of hyperparameters for my Keras model.

### Hyperparameters Tuned

The following hyperparameters are tuned in the model:

- **Optimizer**: The optimizer determines how the model is updated based on the loss function. I test three different optimizers:
  - `adam`
  - `rmsprop`
  - `sgd`

- **Activation Function**: The activation function introduces non-linearity into the model. I evaluate:
  - `relu`
  - `tanh`

- **Number of Neurons**: This specifies the number of neurons in the hidden layer, affecting the model's capacity to learn patterns. I test three configurations:
  - 10 neurons
  - 20 neurons
  - 30 neurons

- **Batch Size**: This parameter defines the number of samples processed before the model is updated. I explore:
  - Batch size of 5
  - Batch size of 10

- **Epochs**: The number of times the learning algorithm will work through the entire training dataset. I try:
  - 10 epochs
  - 20 epochs

### Grid Search

I employ `GridSearchCV` from Scikit-Learn to perform an exhaustive search over the specified hyperparameter values. The process involves:

1. Defining a grid of hyperparameter values to search.
2. Splitting the training data into multiple folds for cross-validation.
3. Training the model on different combinations of hyperparameters.
4. Evaluating the model performance using accuracy as the scoring metric.

### Output

After running the Grid Search, I print the best hyperparameters, providing insights into which combination yielded the highest accuracy on the validation dataset. This information is essential for further refining the model before final evaluation on the test set.

By systematically tuning hyperparameters, I aim to enhance the model's predictive performance and generalization ability.