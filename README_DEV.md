When you start to work on this:

- in console run: 

// if you're just joining the project, try
install.packages('renv')

# this will restore libraries
renv::restore()

# this will create a new record which can be restored. Choose 2: Install the packages, then snapshot.
renv::snapshot()



//but probably you do just this
renv::rebuild()


//only first time (try first without this)
renv::init() 
then pick 'reactivate (2)'


//?renv::activate()

- then in R studio use the button Render.

