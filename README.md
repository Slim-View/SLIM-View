# ADDITIONAL Comparison with related work PrivSyn

**PrivSyn: PrivSyn: Differentially Private Data Synthesis**
**Authors: Zhikun Zhang, Tianhao Wang, Ninghui Li, Jean Honorio, Michael Backes, Shibo He1, Jiming Chen, Yang Zhang**
**In 30th USENIX Security Symposium (USENIX Security 21) (pp. 929-946)**

![alt text](https://github.com/Slim-View/SLIM-View/codaspy-Experiments-PrivSyn.png?raw=true)
In the above figure, we show a comparison of our proposed method SLIM-View with PrivSyn. For the sake of this comparison we generated 6 random range queries workload (size 100) with dimension from 2 to 6 (for each dataset).

For each of these workloads, we created the corresponding dataset and passed it to each method (workload + tensor) for evaluation. Each evaluation was repeated 10 times, and we utilized the same hyperparameters for SLIM-View as presented in the paper. For both methods, we set the epsilon value to $\epsilon = 0.1$.

Based on the results depicted in the figure, our solution consistently outperforms PrivBayes by a significant margin in all conducted tests. This indicates that PrivSyn, much like PrivBayes, struggles to generate high-quality synthetic data when the input data is pre-aggregated into a count-tensor. This count-tensor possesses a specific attribute 'Measure' that captures the count of aggregated data, and the count queries on this data are performed based on this attribute: select sum(Measure) where Range.

The code in this directory is provided for reproducing the results.

