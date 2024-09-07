
# Facial Recognition Quantum System

## Overview

This project implements a sophisticated facial recognition system using both classical and quantum algorithms. The system includes classical deep learning models (e.g., CNN-LSTM) and quantum machine learning models (e.g., Quantum k-NN, Quantum SVM) to recognize faces and process spatial, temporal, and contextual features.

## Directory Structure

```
facial-recognition-quantum/
│
├── data/                     # Raw and processed data
├── models/                   # Classical and quantum models
├── notebooks/                # Jupyter notebooks for model development
├── quantum/                  # Quantum utilities and simulators
├── scripts/                  # Scripts for data splitting, training, and evaluation
├── configs/                  # Configuration files for classical and quantum models
├── utils/                    # Utility functions for data preprocessing, metrics, and visualization
├── results/                  # Confusion matrices, predictions, and evaluation results
├── logs/                     # Training logs and checkpoints
└── README.md                 # Project documentation
```

## Getting Started

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/facial-recognition-quantum.git
   cd facial-recognition-quantum
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install Qiskit for quantum computing:
   ```bash
   pip install qiskit
   ```

### Running the Classical Model

1. Prepare your dataset by placing images in the `data/raw` directory.
2. Split the dataset into training and testing sets:
   ```bash
   python scripts/data_split.py --source_dir=data/raw --train_dir=data/train --test_dir=data/test
   ```
3. Train the classical CNN-LSTM model:
   ```bash
   python scripts/train_model.py --train_dir=data/train --val_dir=data/val --num_classes=10 --epochs=50
   ```

### Running the Quantum Model

1. Prepare a quantum dataset.
2. Train the Quantum k-NN model:
   ```bash
   python scripts/train_quantum_model.py --train_dir=data/train --num_classes=10
   ```

## Configuration

The models can be configured using the YAML files in the `configs/` directory:
- `config_classical.yaml`: Configuration for classical models
- `config_quantum.yaml`: Configuration for quantum models

## Visualization

You can visualize training results and evaluation metrics using the following utilities:
- Confusion matrix plotting
- Training accuracy/loss curves

## Contributing

Contributions are welcome! Please submit a pull request or open an issue.

## License

This project is licensed under the MIT License.
