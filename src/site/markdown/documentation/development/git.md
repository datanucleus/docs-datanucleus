<head><title>Git Usage</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## DataNucleus Source Code : GitHub
![GitHub](../../images/GitHub-Mark-64px.png)

DataNucleus source code is hosted on [GitHub](https://github.com/datanucleus) and uses the [Git](http://git-scm.com/) 
(distributed) source code version control system. You can check out from GitHub using the following.

	Using SSH: git clone git@github.com:datanucleus/{repository-name}.git

	Using HTTPS: git clone https://github.com/datanucleus/{repository-name}.git

Obviously, not everyone will want to check out all DataNucleus project repositories, so use this command for the particular 
repositories that you require. Note that GitHub repositories are all browsable via the web, for example 
[the DataNucleus Neo4j datastore plugin](https://github.com/datanucleus/datanucleus-neo4j).
Note that all plugin repositories are [Maven projects](http://maven.apache.org) so you need to understand how to build 
with Maven to build these plugins.

### Branches

With Git, you use a branch by typing `git checkout {branch_name}`. So for example if I have checked out "datanucleus_core"
then I can switch (from _master_ branch) to the _3.2_ branch by typing `git checkout "3.2"`. Thereafter I'm working on 3.2. To
to back to _master_ just do `git checkout master`.

### Committing changes

Let's say I'm working on my local copy and have made some changes. I now want to commit them (to my local Git repo), so I do
`git commit -a -m "{commit message}"`. This then saves my changes in the local Git repo.

I now want to copy these changes onto GitHub (for others to see). I do `git push git@github.com:datanucleus/{repo_name}.git {branch_name}`.
The changes will then appear immediately on GitHub.