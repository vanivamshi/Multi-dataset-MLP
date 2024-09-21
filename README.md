# Multi-dataset-MLP
Extracts features from multiple support (related) datasets. Their outputs are combined for the main dataset's final output layer to improve performance

Features of the MLP Implementation

1) ReLU Activation Function
2) Residual Connections - The model incorporates residual connections within the main dataset's forward pass to improve gradient flow and mitigate vanishing gradient problems.
3) Support Datasets - The model supports three additional datasets (X_support1, X_support2, X_support3), each with its own set of weights for the hidden layer. Outputs from these support datasets are concatenated and used to enhance the main dataset's processing.
4) Cross-Connections - The model includes weights (W_support_to_main) that connect the combined outputs of the support datasets to the main dataset, allowing information from the support datasets to influence the main dataset.
5) Weight Initialization - Weights for the main and support datasets are initialized using He initialization, which scales the weights by the square root of the number of input units to improve convergence.
6) Forward Propagation - The forward pass involves computing activations for the main dataset and support datasets, combining their outputs, and then applying a residual connection before producing the final output.
7) Backpropagation - The backward pass computes gradients for the main dataset's weights and biases, as well as biases for the support datasets. Weight updates for the main dataset are performed using the calculated gradients, while biases for the support datasets are updated separately.

Modified mathematica equations are given belo.
![1](https://github.com/user-attachments/assets/26a77819-1efd-47ad-b964-6fcfe1e55dbd)
![2](https://github.com/user-attachments/assets/9e7cba8c-c188-45ee-b9a5-61b9006b466b)
![3](https://github.com/user-attachments/assets/c083db78-7bf4-4a33-aa48-38047de01a26)
