When you start to work on this:

- in console run: 

// if you're just joining the project, try
install.packages('renv')

# this will restore libraries. you might wanna do this after pulling.
renv::restore()

# (if you added new libraries) this will create a new record which can be restored. Choose 2: Install the packages, then snapshot.
renv::snapshot()
# of if drama:
renv::rebuild()


# only first time (try first without this). then pick 'reactivate (2)'
renv::init() 


- then in R studio use the button Render.

