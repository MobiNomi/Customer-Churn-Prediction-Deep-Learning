🧠 Customer Churn Prediction Using Deep Neural Network
📌 Model Architecture

The neural network was built using TensorFlow/Keras with the following structure:

🔹 Hidden Layers

Layer 1 → 64 neurons, activation = tanh, L2 regularization (0.001)

Layer 2 → 32 neurons, activation = tanh, L2 regularization (0.001)

Layer 3 → 16 neurons, activation = tanh, L2 regularization (0.001)

Layer 4 → 10 neurons, activation = tanh, L2 regularization (0.001)

🔹 Output Layer

1 neuron

Activation = sigmoid

Used for binary classification (Exited = 0 or 1)

🔹 Regularization

L2 regularization (λ = 0.001) was applied to hidden layers to reduce overfitting by penalizing large weights.

⚙️ Training Configuration

Optimizer: Adam

Learning Rate: 0.005

Loss Function: Binary Crossentropy

Batch Size: 32 (Mini-Batch Gradient Descent)

Epochs: 150

Validation Split: 10% of training data

Data was shuffled at every epoch to improve generalization.

📊 Training Performance
Final Epoch (Training Only)

Training Loss: 0.3612

Training Accuracy: 0.8576

Full Training Set Evaluation

Training Loss: 0.3593

Training Accuracy: 0.8636

Test Set Performance

Test Loss: 0.3587

Test Accuracy: 0.8665

📈 Classification Performance
🔹 Training Set Metrics

Accuracy: 0.8636

Precision: 0.8116

Recall: 0.4307

F1-Score: 0.5627

Confusion Matrix (Train)
[[6207  163]
 [ 928  702]]

This shows:

Model predicts class 0 very well

Recall for churn class (1) is relatively low (43%)

🔹 Test Set Metrics

Accuracy: 0.8665

Precision: 0.8182

F1-Score: ~0.7475 (macro average)

Performance between training and test sets is very close, indicating:

✅ Good generalization
❌ No severe overfitting

🧠 Model Diagnosis

Training accuracy ≈ Test accuracy

Loss values are very similar

This indicates:

✔ Balanced bias-variance tradeoff
✔ No major overfitting
✔ Model generalizes well

However:

Recall for churn class is relatively low, meaning:

Model is conservative in predicting churn

Could be improved using class weights or threshold tuning

🔍 Key Observations

L2 regularization helped stabilize training.

Mini-batch gradient descent improved convergence.

Validation monitoring ensured proper generalization.

Accuracy alone is not sufficient — recall and F1-score provide deeper insight.
