# MML-Paper-03
## Introduction
This repository containts the Python code necessary to recreate the results (regarding the short quantitative analysis) found in the presentation by the [private investigators](https://colinraffel.com/blog/role-playing-seminar.html) in the [MML seminar](https://scoop.iwr.uni-heidelberg.de/teaching/2023ws/seminar-mathematical-machine-learning/) on December 05th 2023.

Some values have to user specified. Thes are marked by comments of the form "**# USER-INPUT**".

Given a set of authors, we calculate quantitative measures of collaboration and provide visualizations.

The notebook was made with the paper _"Understanding deep learning (still) requires rethinking generalization"_ and the corresponding authors Chiyuan Zhang, Samy Bengio, Benjamin Recht, Moritz Hardt and Oriol Vinyals in mind. It should theoretically work for any set of authors, but I have only tested it for the aforementioned authors.

## Algorithm
1. Download the publication data for each author from Google Scholar using scholarly.
2. Create a dictionary of titles with the corresponding authors from our group.
3. Tidy up the data by removing different versions.
4. Calculate collaboration measures.
5. Visualize.

## Notes
If you want to use the notebook for other sets of authors, you have to change the names and ids (which you can find in the URL of the corresponding Google Scholar page) given to the variables `authors` and `author_ids`. Often, the data has to be tidied up, which has to be done manually. We provide some help by first sorting the titles alphabetically and restricting the comparison to pairs of title with small Levenshtein distance.

Also, since Google Scholar does not have a public API (at least to my knowlege), we used the third party Python module scholarly. Since we also used the proxy functionality by scholarly (which is recommended to not get blocked by Google Scholar) retriving the data takes quite some time.

# TODO
* Provide the possibility to save data locally or in Google Drive, thus saving time (since we don't have to reload the Google Scholar data)
* Automate and enhance the tidying up-process
* Create coincidence matrices for conferences
