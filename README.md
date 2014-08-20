
# Redesigning www.novametricsllc.com

The staging (gh-pages) branch is <a href="http://pbogden.github.io/bootstrap">here</a>.  This is what the production site will look like.

The development (gh-pages) branch is <a href="http://eliza-908.github.io/bootstrap">here</a>.  This is what the staging branch will look like.

The old design is <a href="http://pbogden.github.io/bootstrap/oldesign.html">here</a>.

## Collaboration workflow

We're using the <a href="https://help.github.com/articles/using-pull-requests">fork & pull model</a>
for collaborative development.

The development repo will be a <a href="https://help.github.com/articles/fork-a-repo">fork</a> of the staging repo.

Pull requests initiated from the development branch will
<a href="https://help.github.com/articles/merging-a-pull-request">merged</a> with the staging branch,
then migrated to the production site.

The development branch should be up to date before initiating a pull request.
If a pull request requires modification before merging, then migration to production will only occur if 
the staging and development repos are in <a href="https://help.github.com/articles/syncing-a-fork">sync</a>
with those modifications.

####Configuration

The staging repo should be <a href="https://help.github.com/articles/configuring-a-remote-for-a-fork">
configured as the upstream remote</a> for the development branch. 

####Get latest copy of the "origin" == pbogden/bootstrap

    git pull origin master
    git pull origin gh-pages

####Make a new branch for development starting at current HEAD

    git branch my-dev-branch

####Start developing new branch

    git branch                   (list branches)
    git checkout my-dev-branch
 
####Merge a file (dev-file.txt) from the development branch 

    git checkout gh-pages
    git checkout my-dev-branch dev-file.txt
