# Overview
- Graph-Neural-Networks (GNN) represents a given graph where the nodes are linked with edges into a vector space. The typed dependency of given text forms triples of words and dependency (t<sub>dep</sub>, dependency, t<sub>gov</sub>) is similar to the triples of nodes and edge in a graph (n<sub>i</sub>, edge, n<sub>j</sub>). Therefore, this project aims to develop dependency-graph-convolutional-networks in order to represent the dependency relations of each word from given text. The output of the dependency-graph-convolutional-networks is the token-level representation of the sum of the token and its dependency.

# Brief description
- DepGCN.py
> Output format
> - output: The sum of token embedding itself and dependency relation that is connected to the governor. (list)
- text_processing.py
> Output format
> - input_tk_list (list): Tokens of given text based on the selected nlp pipeline.
> - input_dep_list (list): Dependency triple of given text based on the selected nlp pipeline.

# Prerequisites
- argparse
- torch
- stanza
- spacy

# Parameters
- nlp_pipeline(str, defaults to "stanza"): NLP preprocessing pipeline.
- reverse(bool, defaults to True): Applying reverse dependency cases (gov -> dep) or not.

# References
- Graph Neural Networks: Scarselli, F., Gori, M., Tsoi, A. C., Hagenbuchner, M., & Monfardini, G. (2008). The graph neural network model. IEEE transactions on neural networks, 20(1), 61-80.
- Survey of Graph Neural Networks: Zhang, S., Tong, H., Xu, J., & Maciejewski, R. (2019). Graph convolutional networks: a comprehensive review. Computational Social Networks, 6(1), 1-23.
