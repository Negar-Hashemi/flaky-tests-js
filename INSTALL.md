# INSTALL

No specific installation is needed. We provide a single script to extract commits from the top JavaScript projects.

Running the script `script/get_commits.html`, will extract the repositories and commits from GitHub by using the GitHub API. The script contain the following options:

* **Repository**: shows all JavaScript repositories in GitHub, ordered by the star rating.
* **Commits**: by using a name of one of the repositories and selecting one of the keywords, then clicking on the *commits* button will show the list of all commits with the specific keywords obtained from the selected repository.

*Note*: GitHub API has a limit of 30 commits per request. For such repositories, we used manual paginations to extract all commits and saved the extracted commits into a CSV file.
