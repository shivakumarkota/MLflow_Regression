# MLflow_Regression
Steps for MLflow:

Create & activate virtual environment
Create params.yaml
Create .py files for the project or algorithm(get.py,train.py,read params.py)
Use ml flow run method and track metrics and parameters of model
Set tracking uri
Run the code using python  train.py
create MLproject file to package the code
use mlflow run command to run the project using MLproject file. This can be run on any machine.
  mlflow run sklearn_elasticnet_wine -P alpha=0.5
 - Note: you can upload the bundle (i.e MLproject file, code files) to git and  directly run using mlflow run git/... command to run the code on any machine.
-   you can use conda environment along with MLproject file to create a env and run.
-  if conda is not present or you want to run without conda you can use --no-conda flag with mlfow run command
-mlflow run --no-conda sklearn_elasticnet_wine -P alpha=0.5

you can serve the model using mlflow  serve command
e.g: mlflow models serve -m /Users/mlflow/mlflow-prototype/mlruns/0/7c1a0d5c42844dcdb8f5191146925174/artifacts/model -p 1234
Note if you want run with no conda use this command :mlflow models serve --no-conda -m /Users/mlflow/mlflow-prototype/mlruns/0/7c1a0d5c42844dcdb8f5191146925174/artifacts/model -p 1234
