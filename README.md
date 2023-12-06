# MML-Paper-03
## Introduction
This repository containts the Python code necessary to recreate the results (regarding the short quantitative analysis) from the presentation by the private investigators in the MML seminar on December 05th.

Given a set of authors, we calculate quantitative measures of collaboration and provide visualizations.

The notebook was made with the paper "Understanding deep learning (still) requires rethinking generalization" and the corresponding authors Chiyuan Zhang, Samy Bengio, Benjamin Recht, Moritz Hardt and Oriol Vinyals in mind. It should theoretically work for any set of authors, but I have only tested for the aforementioned coauthors.

## Notes
If you want to use the notebook for other sets of authors, you have to change the names and ids (which you can find in the URL of the corresponding Google Scholar page) in the variables ***authors*** and ***author_ids***. Often, the data has to be tidied up, which has to be done manually. We provide some help by first sorting the titles alphabetically and restricting the comparison to pairs of title with small Levenshtein distance.

Also, since Google Scholar does not have a public API (at least to my knowlege), we used the third party Python module scholarly. Since we also used the proxy functionality by scholarly (which is recommended to not get blocked by Google Scholar) retriving the data takes quite some time.

# TODO
* Provide the possibility to save data locally or in Google Drive, thus saving time (since we don't have to reload the Google Scholar data)
* Automate and enhance the tidying up-process
* Create coincidence matrices for conferences
