# README

This is the artifact for the paper:

    Negar Hashemi, Amjed Tahir and Shawn Rasheed, "An Empirical Study of Flaky Tests in JavaScript", In Proceedings of 38h IEEE International Conference on Software Maintenance and Evolution (ICSME 2022)

In this paper, we study causes of and the responses to flaky tests in popular open-source JavaScript projects. Our full artifact package (including scripts used and data files) is available on Zenodo ([![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6673741.svg)](https://doi.org/10.5281/zenodo.6673741)
) ([download from here](https://zenodo.org/record/6673741)).

The artifact package contains the following:

1. **./Data/..**
  + **JavaScript-flakyTests-dataset.csv**: contains our full, unfiltered dataset as extracted form GitHub. It contains 735 commits extracted from the top 40 starred GitHub JavaScript projects, with the name of the repository, commit URL, and the keyword(s) used in the commit.
  * **JavaScript-flakyTests-classification.csv**: contains the set of 481 commits extracted from 18 JavaScript GitHub projects that are found to be true positive (i.e., flaky-related commits), with the following information:
    - *Repository name*.
    - *Commit URL/ID*.
    - *Keyword*: flakiness-related keywords found in the commit message.
    - *Cause of flakiness*.: as found through our manual analysis, see section III.C in the paper.
    - *Response*: the developers' response regarding the flaky test, see section IV.B in the paper.
    - *Type of change*: as whether if the change has resulted in a fix of flakiness or a reduced the occurrence of flakiness .
    - *Type of change*: information of where the change was done to deal with flakiness: 1) test code, or 2) the code under test.

2. **./Script/..**
  * **get_commits.html**: script used with GitHub API to extract commits that contain at least one of the search keywords. Note that GitHub API has a limit of 30 commits per request. For such repositories, we used manual paginations to extract all commits and  saved the extracted commits into a CSV file.
  * **keyword.txt** contains the list of flaky-tests keywords using in our analysis.
