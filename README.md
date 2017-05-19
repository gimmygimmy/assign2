
Please also read the [FAQ] 
https://github.com/gimmygimmy/assign2/blob/master/FAQ.txt


# Python Dependencies

The submission scripts depend on the presence of 2 python packages - `requests` and `future`. If you are missing either of these packages, install them from the online Python registries. The easiest way to do this is through pip:

`pip install requests future`

(assuming develop is the name of your branch)


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
