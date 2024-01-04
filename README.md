# Deep-Learning-based-Credit-Card-Fraud-Detection-Model-with-Human-Expert-Active-Learning

The dataset utilized in this project is the "Credit Card Fraud Detection" dataset from Kaggle, provided by the Machine Learning Group of ULB (Université Libre de Bruxelles). It comprises transactions made by European cardholders in September 2013. This dataset is particularly notable for its high imbalance, as fraudulent transactions represent only 0.172% of all transactions

**Advanced Neural Network Implementation**

The deep learning model is structured around a Sequential neural network with a configuration tuned to address the binary classification challenge presented by fraud detection. Key components of the model include:

•	Dense Layers: These layers serve as the main building blocks of the neural network, with varying neuron counts to facilitate the learning of complex representations from the data.
•	Batch Normalization: This technique normalizes the input layer by adjusting and scaling the activations, which helps mitigate the problem of internal covariate shift, thus speeding up training and improving the stability of the neural network.
•	Dropout: Dropout layers are introduced as a form of regularization to reduce overfitting. By randomly setting a fraction of input units to 0 at each update during training, they help prevent complex co-adaptations on training data.
•	Activation Functions: The 'Relu' function is used for intermediate layers to introduce non-linearity, while the 'sigmoid' function is employed in the output layer to map predictions to a probability distribution suitable for binary classification.
•	Compilation Parameters: The model uses binary cross-entropy as the loss function, appropriate for a binary classification problem. The Adam optimizer is selected for its efficient computation and low memory requirement, along with 'accuracy' as the performance metric.

**Active Learning Implementation**

The project integrates an active learning workflow to improve model performance through expert intervention iteratively:
•	Simulated Expert Review: A function simulates the expert review process, generating corrected labels for the model to learn from, thereby mimicking real-world scenarios where experts provide feedback.
•	Interactive Data Point Review: A manual process allows for the precise updating of labels by human experts, drawing on their domain knowledge to correct model predictions and guide the learning process.

**Training and Evaluation**

•	Handling Class Imbalance: The Synthetic Minority Over-sampling Technique (SMOTE) was applied to address the imbalance issue prevalent in the dataset, thereby enhancing the model's ability to identify the minority class.
•	Training Regimen: The model was trained over 10 epochs with a batch size of 32, a decision based on preliminary experiments to balance training time and model performance.
•	Performance Metrics: A suite of metrics, including accuracy, precision, recall, and the F1 score, were utilized to provide a holistic evaluation of the model's performance. These metrics are particularly relevant for the imbalanced classification task at hand, offering insights into the model's ability to predict minority class instances without overwhelming false positives correctly.


