# ADDITIONAL Comparison with related work PrivSyn

**PrivSyn: Differentially Private Data Synthesis**
**Authors: Zhikun Zhang, Tianhao Wang, Ninghui Li, Jean Honorio, Michael Backes, Shibo He1, Jiming Chen, Yang Zhang**
**In 30th USENIX Security Symposium (USENIX Security 21) (pp. 929-946)**


Each method ( Slim-View, Slim-View WW and PrivSyn) was evaluated using our datasets and workloads.
Datasets used in this experiment : 

  1- Name: Adult, dimensions: 15, number of rows: 48.000
  
  2- Name: Electricity, dimensions: 8, number of rows: 45.000
  
  3- Name: Bitcoin, dimensions: 9, number of rows: 2.916.697
  
For the sake of this comparison we generated 6 workloads each containing 100 random range queries from 2 to 6 dimensions applied to all datasets.
For each of these workloads, we created the corresponding dataset and passed it (workload + tensor) to each method (Slim-View, Slim-View WW and PrivSyn)  for evaluation. Each evaluation was repeated 10 times, and we utilized the same hyperparameters for SLIM-View as presented in the paper ($𝑎𝑙𝑙𝑜𝑐_{prop} = 0.5,sample_{prop} = 0.25$ and $\lambda = 0.05 $). For both methods, we set the epsilon value to $\epsilon = 0.1$.

![alt text](https://github.com/Slim-View/SLIM-View/blob/main/codaspy-Experiments-PrivSyn.png?raw=true)
In the figure above, we show a comparison of our proposed method SLIM-View with PrivSyn.
Based on the results depicted in the figure, our solution consistently outperforms PrivSyn by a significant margin in all conducted tests. This indicates that PrivSyn, much like PrivBayes, struggles to generate high-quality synthetic data when the input data is pre-aggregated into a count-tensor. This count-tensor possesses a specific attribute 'Measure' that captures the count of aggregated data, and the count queries on this data are performed based on this attribute: select sum(Measure) where Range.

The code in this directory is provided for reproducing the results.

