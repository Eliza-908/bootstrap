
## Redesigning www.novametricsllc.com

The staging (gh-pages) branch is <a href="http://pbogden.github.io/bootstrap">here</a>.  This is what the production site will look like.

The development (gh-pages) branch is <a href="http://eliza-908.github.io/bootstrap">here</a>.  This is what the staging branch will look like.

The old design is <a href="http://pbogden.github.io/bootstrap/oldesign.html">here</a>.

## Development workflow

We're using the <a href="https://help.github.com/articles/using-pull-requests">fork & pull model</a>
for collaborative development.

The development repo is a <a href="https://help.github.com/articles/fork-a-repo">fork</a> of the staging repo.

Pull requests initiated from the development branch will be
<a href="https://help.github.com/articles/merging-a-pull-request">merged</a> with the staging branch,
then migrated to the production site.

The <a href="https://github.com/eliza-908/bootstrap">development repo</a> should be up to date 
before initiating a pull request.

If a pull request must be modified before merging, then migration to production will only occur after
the staging and development repos are in <a href="https://help.github.com/articles/syncing-a-fork">sync</a>
with those modifications.

####On staging repo...

######Checkout pull request

    git checkout -b Eliza-908-gh-pages gh-pages                (create a *new* branch)
    git checkout Eliza-908-gh-pages                            (...or if that branch exists)
    git pull git@github.com:Eliza-908/bootstrap.git gh-pages   (get pull request)

######Compare two branches

    git diff gh-pages..Eliza-908-gh-pages

######Merge changes and update and update github

    git checkout gh-pages
    git merge --no-ff Eliza-908-gh-pages
    git push origin gh-pages

######Delete a dev branch

    git branch -d Eliza-908-gh-pages  (local)
    git push origin :Eliza-908-gh-pages (github) 


####On development repo...

######Configure upstream remote

The staging repo should be <a href="https://help.github.com/articles/configuring-a-remote-for-a-fork">
configured as the upstream remote</a> for the development branch. 

    git remote -v     (list current remote)
    git remote add upstream https://github.com/pbogden/bootstrap.git
    git remote -v     (verify new configuration -- see <a href="https://help.github.com/articles/configuring-a-remote-for-a-fork">docs</a>)

######Sync fork with upstream remote

    git fetch upstream
    git checkout master
    git merge upstream master
    git checkout gh-pages
    git merge upstream gh-pages

######Make a new branch for development/testing starting at current HEAD

    git branch my-dev-branch

######Start developing/testing a new branch

    git branch                   (list branches)
    git checkout my-dev-branch
 
######Merge a file (dev-file.txt) from a development/testing branch 

    git checkout gh-pages
    git checkout my-dev-branch dev-file.txt
