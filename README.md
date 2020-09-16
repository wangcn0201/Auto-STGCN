# Auto-STGCN
An automated system for STGCN model development.

## 1. Auto-STGCN Algorithm: Searching for the optimal STGCN model
`Inputs`<br>
* Dataset name, Dataset partition ratio (validation set, test set, training set), Input sequence length, Output sequence length,<br>
* Timemax, Epoch size of each candidate model,<br>
* Initial epsilon, Epsilon reduce step, Epsilon decay Ratio, Gamma of Qlearning, Learning rate of Qlearning, Episodes of Qlearning<br>

`Outputs`<br>
* Code and performance scores of the Optimal STGCN searched by Auto-STGCN<br>
* Log info of Auto-STGCN<br>

`Command`<br>
python Qlearning.py --Data "PEMS03"
python Qlearning.py --Data "PEMS03" --gamma 0.1
