# Auto-STGCN
An automated system for STGCN model development.<br>
Code for paper 'Auto-STGCN: Autonomous Spatial-Temporal Graph Convolutional Network Search Based on Reinforcement Learning and Existing Research Results'.<br>

## 1. Auto-STGCN Algorithm: Searching for the optimal STGCN model
### Files
Auto_STGCN.py --- run Auto-STGCN akgorithm<br>
Model.py --- build STGCN model according to code<br>
Env.py --- read dataset, record the state-action-reward information in Auto-STGCN algorithm<br>
ExperimentDataLogger.py --- output the log information of Auto-STGCN algorithm<br>
/Log --- log files<br>
/utils --- auxiliary files<br>
/data --- datasets<br>
/Config --- default configurations<br>

### Inputs
* Dataset name, Dataset partition ratio (validation set, test set, training set), Input sequence length, Output sequence length,<br>
* Timemax, Epoch size of each candidate model,<br>
* Initial epsilon, Epsilon reduce step, Epsilon decay Ratio, Gamma of Qlearning, Learning rate of Qlearning, Episodes of Qlearning<br>

### Outputs
* Code and performance scores of the Optimal STGCN searched by Auto-STGCN<br>
* Log info of Auto-STGCN<br>

### Command
* `python Auto_STGCN.py --Data "PEMS03"`<br>
* `python Auto_STGCN.py --Data "PEMS03" --gamma 0.1`<br>

## 2. Auto-STGCN Algorithm: Training the optimal STGCN model
### Inputs
* Optimal STGCN code, Dataset name, Dataset partition ratio (validation set, test set, training set), Input sequence length, Output sequence length,<br>
* Model training epochs, Model training times,<br>
* Load model weight = None<br>

### Outputs
* Performance scores (Mean + variance: MAE, MAPE, RMSE, Time) of the Optimal STGCN model<br>
* Log info of the model training<br>

### Command
* `python TestBestSTGNN.py --model "...." --Data "PEMS03" --Load "None"`<br>
* `python TestBestSTGNN.py --model "...." --Data "PEMS03" --Load "None"`<br>
