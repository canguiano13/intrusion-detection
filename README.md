
# Anomaly Detection in Network Traffic

In this project, we implement a number of machine learning models for detection of anomalous network traffic. To achieve this, we train both supervised and unsupervised models against the 1999 KDDCup dataset.

## Prerequisites
### i. Virtual Environment
Our implementation makes use of several libraries in order to execute a number of vital dataprocessing and model training tasks. These libraries are listed in the `requirements.txt` file. The required libraries can be installed using the following command:

`pip install -r requirements.txt`

or, if you do not want to use the requirement file:

`pip install numpy pandas seaborn scikit-learn mlxtend imbalanced-learn`

It is recommended to install these libraries into a virtual environment. More information about creating and using virtual environments is available [here](https://docs.python.org/3/library/venv.html).

If you instead prefer to use  a Conda-based environment, you will need to run the following:

`conda env create -f environment.yml` (first time only) \
`conda activate kdd-env` \
`code .`  (opens VS Code inside the env)             


### ii. Obtaining the Dataset
This project makes use of the 1999 KDDCup dataset. As a result, it is required to have the `kddcup.data.gz` and `kddcup.names.txt` files in the project's root folder. If these files do not exist in your project folder, they can be obtained online via the [official KDDCup99 dataset page](https://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html).

## Implementation

### 1. Overview
Our notebook, `final.ipynb`, does the following:
1. Loads the KDDCup99 dataset and performs a basic exploration of the dataset.
2. Performs data processing to appropriately encode and standardize data.
3. Trains multiple anomaly detection models. \
    a. Visualizes model outcomes. \
    b. Evaluates each model using accuracy, precision, and recall.
4. Evaluates overall performance in comparison to other models. 

### 2. Models Implemented
Our notebook implements the following models:

- Supervised:
  - Decision Tree
  - Random Forest
- Unsupervised:
  - K-Means Clustering
  - Isolation Forest

### 3. Evaluation
To evaluate the performance of our models, we used the accuracy, precision, and recall scores. When possible, we trained our models to emphasize recall performance, as we feel this is vital to obtain a model that can identify anomalous traffic confidently and reliably.

### 4. How to Run this Notebook
1. Open the notebook using Jupyter or Visual Studio Code.
2. Run all cells (Kernel > Restart & Run All).

