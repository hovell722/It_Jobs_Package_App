# IT Jobs Watch Data with DEV-ENV

## Introduction
The aim of this project is to create a simple service that can scrape useful data from ITJobswatch.

## Current Scope
At present the app is set up to be cloned and used to simply scrape the below services:

1. Home page top 30 job/roles / skills which can be found [here]()

The aim will be to expand this to further services such as:

* Regular polling of pages and writing to a database for longer terms stats
* Bespoke calls for specific job role data

And much more.

## Getting started with the code and contributing
```
1) Clone the Repo
2) The code is inside it_jobs_watch_code.
3) Make changes and commit to dev branch.
```

### Trigger the CI and merger code

1) create a dev branch `dev-*`
2) Commit changes
3) Make pull request

The pull request Trigger CI.


### Feedback from CI
If your code clears the test, you can get the results on your Teams Channel.

## Usage and testing in VM

To test your code in a CLEAN DEV environment run the vagrant file with this command:

```
vagrant up
```
This will create a VM with only the needed packages and provision the code.

Then ssh into the machine and run the tests:
```
vagrant ssh

python -m pytest test/

```

_Pre-Requisites_
* Pycharm IDE
* Python 3.x + installed

### Installing packages
The necessary packages needed to run this program should automatically be picked up by pycharm. You may find a a few pop ups within the IDE that state there are dependencies missing, if you simply install these through the IDE you should be set up correctly.  

### Running tests

To test whether the program will work from your machine:

 * Ensure the `config.ini` file has the test environment set to `live`
 * Click the `Terminal` icon which can be found on the menu in the bottom left of Pycharm.
* Ensure you're in the root path of the project and type `python -m pytest tests/`

This should execute the tests if any fail you may have issues with this program.

### Running and using the program
To use the program simply right click on the `main.py` file and then click `Run 'main'`. This will run the command line user interface.

Follow the instructions to download via the various options given.



# Next steps
* Adding a job details search option (essentially be able to search for a specific role and return the details in a CSV)
* create a connected database for full deployment
* Build a scheduler as part of a full deployment to poll and add to the database
