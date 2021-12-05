
# Git Hub Social Network Link Prediction

A large [social network of GitHub developers](https://snap.stanford.edu/data/github-social.html) was collected from the public API in June 2019. 
The vertex features were extracted based on the location, repositories starred, employer and e-mail address. 
Link prediction is performed to predict whether pairs of GitHub developers will have mutual followers or not in the future.

## Dataset Description
[git_nodes.csv](https://github.com/TimKong21/Git-Hub-Social-Network-Link-Prediction/blob/main/git_nodes.csv)
- Nodes are developers who have starred at least 10 repositories.
- Each node is binary labelled (web or a machine learning developer).

[git_edges.csv](https://github.com/TimKong21/Git-Hub-Social-Network-Link-Prediction/blob/main/git_edges.csv)
- Edges are mutual follower relationships between the GitHub developer.
- Edges will then be split for training node embeddings and link prediction model.

## Notebook walkthrough
[link prediction.ipynb](https://github.com/TimKong21/Git-Hub-Social-Network-Link-Prediction/blob/main/link%20prediction.ipynb) demonstrate the implementation of the algorithms.

    1. Split graph into training graph and test graph.
    2. Split edges for training link embeddings and link prediction model.
    3. Calculate and save link embeddings for the whole graph.
    4. Reduce dimension and visualize link embeddings on a 2-D scale.
    5. Train link prediction classifier.
    6. Evaluate the classifier on the test data.
## References

 - [SNAP GitHub Social Network](https://snap.stanford.edu/data/github-social.html)
 - [Stellargraph Link prediction with Node2Vec](https://stellargraph.readthedocs.io/en/stable/demos/link-prediction/node2vec-link-prediction.html)
