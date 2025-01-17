# Graph Classification with GIN and GCN with Global Pooling
Project Overview
This project demonstrates graph classification techniques using the Graph Isomorphism Network (GIN) architecture to process and model molecular structures for classification and regression tasks. Specifically, it focuses on molecular datasets, leveraging SMILES strings to build graph representations. The project includes data processing, model implementation with PyTorch Geometric, and a study of ensemble performance combining GIN and Graph Convolutional Network (GCN) architectures.

## Features
- Molecular Data Processing: Includes steps to process SMILES data into graph-compatible formats.
- Classification and Regression: Models both binary classification (HIV activity) and regression tasks (lipophilicity prediction).
- Ensemble Modeling: Tests the performance of combining GCN and GIN architectures.

## Installation

Prerequisites
- Python 3.x
- Jupyter Notebook or Google Colab
- Required packages:
  - torch
  - torch-geometric
  - rdkit
  - ogb

## Installation Steps
1. Clone the repository:
```bash
git clone https://github.com/btarun13/Graph_classification_related.git
cd your-repo-name
```
2. Get code locally or push it to colab
   
3. (Optional) Install additional dependencies if using Google Colab.
   
```bash
# Run in a cell in Colab
!pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-2.2.1+cu121.html
!pip install torch-sparse -f https://pytorch-geometric.com/whl/torch-2.2.1+cu121.html
!pip install torch-geometric
!pip install rdkit
```

## Usage
- Load Data: Ensure the datasets for HIV and Lipophilicity are in your environment or specify their paths. Example datasets can be downloaded from MoleculeNet.
- Data Processing: Convert SMILES data to graph structures suitable for the GIN model.
- Training and Evaluation: Follow the steps in the notebook to train GIN and GCN models, evaluate performance, and explore ensemble approaches.


## Example Commands

- Data loading and preprocessing:

```python
Copy code
hiv_data = pd.read_csv("/path/to/HIV.csv")
lipo_data = pd.read_csv("/path/to/Lipophilicity.csv")
```

- Model Training:

```python
# Train GIN model
gin_model = GINConv(...)
```

- Follow the training steps in the notebook

## Results
The notebook provides an evaluation of:
1. Classification Accuracy for HIV activity prediction.
2. Ensemble Comparison between GIN, GCN, and combined models.
3. Final function would give a probability estimate with SMILE string and model(you use for estimate) Eg. smile_to_hiv_prob(i,best_model).item() == estimate

## Acknowledgments

Special thanks to the creators of the datasets provided by MoleculeNet, and to the developers of PyTorch Geometric and the Open Graph Benchmark (OGB) team.

## License
This project is licensed under the MIT License.



