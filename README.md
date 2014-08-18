
# Redesigning www.novametricsllc.com

The gh-pages (prototype) branch is served <a href="http://pbogden.github.io/bootstrap">here</a>.

The old design is <a href="http://pbogden.github.io/bootstrap/oldesign.html">here</a>.

# Collaboration workflow

We're using the <a href="https://help.github.com/articles/using-pull-requests">fork & pull model</a>
for collaborative development.

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
