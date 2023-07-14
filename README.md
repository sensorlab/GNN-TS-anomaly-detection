# GNN-TS-anomaly-detection

## Rutgers
The Rutgers.ipynb notebook is designed to convert time series data from the Rutgers dataset into graphs. These graphs are categorized into 5 groups, each representing a specific anomaly type. The notebook includes a GINE model for classifying the graphs based on the anomaly types and a GAT model for identifying the nodes where the anomalies occurred within the time series. The datasets were created with Rutgers_dataset_creation.ipynb.

## Rutgers Importance
Rutgers_importance.ipynb is a notebook that builds on Rutgers.ipynb. It calculates importance scores for each node using the gradient method. The importance score can be calculated when the model is trained by sending the test loader through the model and inspecting the gradients. Nodes with higher scores are considered more important. To assess the accuracy of the importance scores, the notebook includes a modified test step where the most important nodes are masked, and the prediction changes are observed. You can choose between the importance calculation method provided by GraphXAI and the one implemented in this notebook.

# How to install and run
All notebooks were run in jupiter hub, except Rutgers_dataset_creation.ipynb that was run in google colab.  
Each of the three main notebooks contains cells at the beginning that install the required versions of the packages.
In each notebook, the cells, with the exception of pip install, Config, and the last main cell, are functions that must be executed before the last cell is executed, which runs the entire program.   
To change the parameters, you can edit the Config Cell located before the last cell in each notebook.

# Citations
@INPROCEEDINGS{10167910,
  author={Bertalanič, Blaž and Vnučec, Matej and Fortuna, Carolina},   
  booktitle={2023 International Balkan Conference on Communications and Networking (BalkanCom)},    
  title={Graph Neural Networks Based Anomalous RSSI Detection},    
  year={2023},   
  volume={},   
  number={},   
  pages={1-5},   
  doi={10.1109/BalkanCom58402.2023.10167910}}   