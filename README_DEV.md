# When you start to work on this you will need to use renv which takes care of the libraries and their versions.

A bit more setup, a much less drama. Cache the project library and global renv cache on the CI service.

In short: from **renv** documentation. In r console:

- Call `renv::snapshot()` on your local machine to generate renv.lock.
- Call `renv::restore()` on your CI service to restore the project library from renv.lock.

Btw. if you're just joining the project, you might need
```
install.packages('renv')
```

## Restore renv.lock

This will restore libraries. you might wanna do this after pulling. Choose "1: Activate the project and use the project library", you might have to do it twice 

```
renv::restore()
```

## (if you added new libraries) this will create a new record which can be restored. Choose 2: Install the packages, then snapshot.

```
renv::snapshot()
```

## of if drama:

```
renv::rebuild()
```

## which is the same as below + picking 'reactivate (2)'

```
renv::init() 
```

- then in R studio use the button Render to have a preview of your work.

