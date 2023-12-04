# MML-Paper-03
## Introduction
This repository containts the Python code necessary to recreate the results from the presentation by the private investigators in the MML seminar on December 05th.

Given a set of authors, we calculate quantitative measures of collaboration and provide visualizations.

The notebook was made with the paper "Understanding deep learning (still) requires rethinking generalization" and the corresponding authors Chiyuan Zhang, Samy Bengio, Benjamin Recht, Moritz Hardt and Oriol Vinyals.

## Notes
If you want to use the notebook for other sets of authors, you have to change the names and ids (which you can find in the URL of the corresponding Google Scholar page) in the variables ***authors*** and ***author_ids***. Often, the data has to be tidied up, which has to be done manually. We provide some help by first sorting the titles alphabetically and restricting the comparison to pairs of title with small Levenshtein distance.

# TODO
* Automatic and enhance the tidying up-process
* Create coincidence matrices for conferences
