
Set up a demo site using Bootstrap

1. Follow the instructions to set up a <a href="https://pages.github.com/">GitHub Pages</a> website

2. Create a new repository, call it "bootstrap"

3. Clone the repository onto your Mac.  If you have xCode installed, then you can type

    git clone git@github.com:pbogden/bootstrap.git
    cd bootstrap

4. Create a file named "index.html" with the following content

    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap 101 Template</title>
    
    <!-- Bootstrap -->
    <link href="css/bootstrap.min.css" rel="stylesheet">
   
    <!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
    <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
    <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
    </head>
    <body>
    <h1>Hello, world!</h1>
    
    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="js/bootstrap.min.js"></script>
    </body>
    </html>

5. Create an orphan branch named gh-pages

    git checkout --orphan gh-pages
    git add .
    git commit -m "first commit to gh-pages branch"
    
6. Push the file to the repository and browse to http://pbogden.github.io/bootstrap


