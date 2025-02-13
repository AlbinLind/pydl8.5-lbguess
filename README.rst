This is a fork of the fork of `dl8.5 <https://github.com/aia-uclouvain/pydl8.5/tree/b9583c8d72d7ca756041e4dafbdc3ffb7fc083eb>`_, which adds lower-bound guessing, as outlined in the paper  `Fast Sparse Decision Tree Optimization via Reference Ensembles <https://arxiv.org/abs/2112.00798>`_. This new fork contains a PEP-517 compliant pyproject.toml for modern python.

**Installation**

``python3 setup.py install``

Note: you may need to manually uninstall dl8.5 with pip if you have used the pip installation of dl8.5 before. 
 
**Differences from dl8.5**

Lower-bound guessing is handled via an extra input `warm`, which would be a vector of the predictions of a reference model for each point in the training set. (label 0 = reference model's prediction was incorrect for this point, 1 = reference model's prediction was correct for this point)

All use cases for dl8.5 from prior to September 2021 are supported, although we currently do not support the use of a reference model with the hyperparameter iterative=true.

**Relevant Papers**

- Aglin, G., Nijssen, S., Schaus, P. Learning optimal decision trees using caching branch-and-bound search. In AAAI. 2020.
- McTavish, H., Zhong, C., Achermann, R., Karimalis, I., Chen, J., Rudin, C., & Seltzer, M. Fast Sparse Decision Tree Optimization via Reference Ensembles. In AAAI. 2022.

Note: This fork was created prior to dl8.5's September 2021 updates to support non-classification tasks.  
