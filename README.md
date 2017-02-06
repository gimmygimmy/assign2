# CS 6601: Artificial Intelligence - Assignment 2, Search

Please also read the [FAQ].
FAQ

Aggregated Feedback + Solutions

1. Setting up for Assignment 2 (written by a student) - https://docs.google.com/document/d/1IJNulLl0fDzZdeJmzOghNC2emh_6QR1zm8vxKTYD0Es/pub

2. If romania = pickle.load(open('romania_graph.pickle', 'rb')) does not work (especially on Windows), you can try reading it without binary mode using romania = pickle.load(open('romania_graph.pickle', 'r')).

3. Use %matplotlib inline if you want to see the plots displayed within the same browser. Add it after the import statements at the top and you should be good.

4. If you have networkx installed and don’t want to use virtualenv, you can try replacing sys.path.append('lib') with sys.path = ['lib'] + sys.path.

5. Make sure you clean up any changes/modifications/additions you make to the networkx graph struture before you exit the search function. Depending on your changes, the auto grader might face difficulties while testing. The best alternative is to create your own data structure(s).

6. If you're having problems (exploring too many nodes) with your Breadth first search implementation, one thing many students have found useful is to re-watch the Udacity videos for an optimization trick mentioned.

7. You may not get full credit if your tri-directional implementation has calls to your bi-directional implementation.

8. While submitting to Bonnie, many times the submission goes through even if you get an error on the terminal. You should check the web interface to make sure it’s not gone through before re-submitting. On the other hand, make sure your final submission goes through with Bonnie. Submit your code to T-Square as a backup.

9. Most 'NoneType object ...' errors are because the path you return is not completely connected (a pair of successive nodes in the path are not connected). Or because the path variable itself is empty.

10. Adding unit tests to your code may cause your Bonnie submission to fail. It is best to comment them out when you submit to Bonnie.

11. The testing file map_test.py is intended as a diagnostic tool. Feel free to modify it, but be careful.

12. Make sure you're returning [] for when the source and destination points are the same.

# Setup
Clone this repository recursively:
`git clone --recursive https://github.gatech.edu/omscs6601/assignment_2.git`

(If your version of git does not support recurse clone, then clone without the option and run `git submodule init` and `git submodule update`).

If you run across certificate authentication issues during the clone, set the git SSL Verify option to false: `git config --global http.sslVerify false`.

# Python Dependencies

The submission scripts depend on the presence of 2 python packages - `requests` and `future`. If you are missing either of these packages, install them from the online Python registries. The easiest way to do this is through pip:

`pip install requests future`

# Keeping your code upto date
After the clone, we recommend creating a branch and developing your agents on that branch:

`git checkout -b develop`

(assuming develop is the name of your branch)

Should the TAs need to push out an update to the assignment, commit (or stash if you are more comfortable with git) the changes that are unsaved in your repository:

`git commit -am "<some funny message>"`

Then update the master branch from remote:

`git pull origin master`

This updates your local copy of the master branch. Now try to merge the master branch into your development branch:

`git merge master`

(assuming that you are on your development branch)

There are likely to be merge conflicts during this step. If so, first check what files are in conflict:

`git status`

The files in conflict are the ones that are "Not staged for commit". Open these files using your favourite editor and look for lines containing `<<<<` and `>>>>`. Resolve conflicts as seems best (ask a TA if you are confused!) and then save the file. Once you have resolved all conflicts, stage the files that were in conflict:

`git add -A .`

Finally, commit the new updates to your branch and continue developing:

`git commit -am "<funny message vilifying Bonnie>"`

# Submit your code
To submit your code to have it evaluated for a grade, use `python submit.py assignment_2`.  You may submit as many times as you like.  The last submission before the deadline will be used to determine your grade.

To add a data.pickle file to your submission (containing landmarks of the Atlanta map for improved tri-directional/custom_search), use `python submit.py assignment_2 --add-data`.

A friendly reminder: please ensure that your submission is in `search_submission.py`. The submit script described automatically sends that file to the servers for processing.

# Vagrant

You have the option of using vagrant to make sure that your local code runs in the same environment as the servers on Bonnie (make sure you have [Vagrant](https://www.vagrantup.com/) and [Virtualbox](https://www.virtualbox.org/wiki/Downloads) installed).  To use this option run the following commands in the root directory of your assignment:

```
vagrant up --provider virtualbox
vagrant ssh
```

Your code lives in the `/vagrant` folder within this virtual machine. Changes made to files in your assignment folder will automatically be reflected within the machine.

# Azure Notebooks

Azure has a service for creating and hosting your iPython notebooks. Find it [here](https://notebooks.azure.com/). You can even use your Georgia Tech credentials to sign in. 
