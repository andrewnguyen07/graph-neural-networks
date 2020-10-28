# Graph Neural Networks

This project shows multiple Jupyter Notebooks which demonstrate a variety of Graph Neural Network models built and tuned to analyze the relationships between Facebook pages (nodes) and to classify unseen data into categories for the [Facebook Large Page-Page Network](https://snap.stanford.edu/data/facebook-large-page-page-network.html). The network is Undirected, with 22k nodes and 171k edges. 

## List of different Graph Models:

* Network Analysis: loaded nodes and edges into the network, set feature variables as node attributes, computed connectivity and centrality metrics of the network.
* GraphSAGE: prepared network by loading nodes and edges, flowed network into StellarGraph network for modelling, generated train and test set with GraphSAGENodeGenerator, which took a sample set of data into modelling. The model achieved the accuracy score of train/test set at 91%/86%.  
* GCN: prepared network similar to GraphSAGE, but generated full-batch train and test set instead of sub-sampling by FullBatchNodeGenerator. The model is conceptualized from the mechanism of CNN in which a kernel of (axb) layer acts as a sliding window across the network to learn features from the node itself but from the neighbors as well. The model achieved the accuracy score of train/test at 92%/86%.
* GAT: similar pre-processing steps as GCN, but GAT model pays more attention to "important neighbors" while sliding through the network with the a kernel of (axb) layer and has better runtime due to attention layers being calculated in parallel. The model achieved the accuracy score of train/test set at 92%/90%, the higest among all models.

## Requirements

* pandas
* numpy
* matplotlib
* seaborn
* sklearn
* tensorflow
* networkx
* stellargraph
