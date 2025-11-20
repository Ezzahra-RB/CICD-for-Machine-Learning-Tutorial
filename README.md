# CI/CD for Machine Learning -- TP Project

This repository contains the implementation of my **Machine Learning
CI/CD pipeline**, inspired by the Datacamp tutorial:\
**"CI/CD for Machine Learning" --
https://www.datacamp.com/tutorial/ci-cd-for-machine-learning**

The goal of this TP is to understand how Continuous Integration and
Continuous Deployment can be applied to ML workflows, from data
preprocessing to model deployment.\
The project includes a drug classification model, automated training and
evaluation scripts, and a GitHub Actions workflow that builds and tests
the pipeline on every update.

## 📁 Project Structure

    CICD-for-Machine-Learning-Tutorial/
    │
    ├── App/                       # Gradio interface for model inference
    │   └── drug_app.py
    │
    ├── Data/
    │   └── drug.csv               # Dataset used for training
    │
    ├── Model/
    │   └── drug_pipeline.skops    # Serialized trained model (artifact)
    │
    ├── Results/                   # Evaluation reports & figures
    │   ├── metrics.txt
    │   └── model_results.png
    │
    ├── .github/workflows/
    │   └── ci.yml                 # Main CI/CD pipeline
    │
    ├── Makefile                   # Commands for install, training, evaluation, formatting
    ├── notebook.ipynb             # Exploratory notebook
    ├── requirements.txt           # Python dependencies
    └── README.md

## 🚀 Getting Started

### 1. Clone the repository

``` bash
git clone <your_repo_link>
cd CICD-for-Machine-Learning-Tutorial
```

### 2. Create a virtual environment

``` bash
python -m venv venv
source venv/bin/activate        # Linux/Mac
venv\Scripts\activate         # Windows
```

### 3. Install dependencies

``` bash
pip install -r requirements.txt
```

## 🧪 Running the Application

### Launch the Gradio Web App

``` bash
cd App
python drug_app.py
```

## ⚙️ CI/CD Workflow (GitHub Actions)

The CI/CD pipeline is defined in `.github/workflows/ci.yml`.

It performs the following tasks automatically:

### Continuous Integration (CI)

-   Install dependencies
-   Format the code (`make format`)
-   Train the model (`make train`)
-   Evaluate the model (`make eval`)
-   Upload trained model and evaluation results

### Continuous Deployment (CD)

-   Optional branch update with latest model artifacts

### Pipeline Triggers

-   Push on `main`
-   Pull request to `main`
-   Manual trigger (`workflow_dispatch`)

## 📊 Results

The pipeline generates: - `metrics.txt` - `model_results.png` -
`drug_pipeline.skops`

## 🧠 What I Learned

-   Applying CI/CD to Machine Learning lifecycle
-   Automating training, evaluation, and artifact tracking
-   Using GitHub Actions for reproducible ML workflows
-   Using Makefiles to standardize commands

## 📚 References

-   https://www.datacamp.com/tutorial/ci-cd-for-machine-learning
-   GitHub Actions Docs

## 📄 License

MIT License
