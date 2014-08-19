
# Redesigning www.novametricsllc.com

The staging (gh-pages) branch is <a href="http://pbogden.github.io/bootstrap">here</a>.  This is what the production site will look like.

The development (gh-pages) branch is <a href="http://eliza-908.github.io/bootstrap">here</a>.  This is what the staging branch will look like.

The old design is <a href="http://pbogden.github.io/bootstrap/oldesign.html">here</a>.

## Collaboration workflow

We're using the <a href="https://help.github.com/articles/using-pull-requests">fork & pull model</a>
for collaborative development.

The development branch will be a <a href="https://help.github.com/articles/fork-a-repo">fork</a> of the staging repo.

Pull requests from initiated from the development branch will be checked and merged with the staging branch.  The development branch should remain in sync with the staging branch.  If a pull request requires modification, then changes will be migrated to production once those changes are in sync with the development branch.

####Get latest copy of the "origin" == pbogden/bootstrap

    git pull origin master
    git pull origin gh-pages

####Make a new branch for development starting at current HEAD

    git branch my-dev-branch

####Start developing new branch

    git branch                   (list branches)
    git checkout my-dev-branch   (may not be necessary)
 
####Merge a file (dev-file.txt) from the development branch 

    git checkout gh-pages
    git checkout my-dev-branch dev-file.txt
