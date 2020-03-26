# template
Template repository that can be cloned within a project folder and used to create a python environment and git repository for that project. It includes the files (README, conda env yml, license, and python gitignore) to initiate a basic conda/git project. Items should be customized before step 3 below (i.e. update the yml file to include whatever python packages you need for reproducible projects *before* executing steps 3-5 below).

1. Clone this repo where ever you want your project to be located.
2. Rename the repo from `template ` to your project/feature name, and then edit the name within in the yml file to match your project name. 
    * The yml file is used to create a python environment, and so editing the name (first line), packages, and environment location (last line) in the yml file should be necessary every time you start a new project.
3. Fire up conda and change directory to the project directory. Then create a conda environment, activate the environment, push the repository to Github, then push the master branch. 

    All together using `conda`:

        $ mkdir new_project
        $ cd new_project
        $ conda env create
        $ source activate template
        $ git create
        $ git push -u origin master

Alternatively, if we wanted to specify the location of the python environment without using the yml file (deleting the line from the file), then we could do the following instead:

    $ mkdir new_project
    $ cd new_project
    $ conda create --prefix env # creates a new environment directory `env` in the current directory
    $ conda activate ./env
    $ git init
    $ git commit -m "Initial commit"
    
## Updating your environment
You may need to update your environment for a variety of reasons. For example, it may be the case that:

* one of your core dependencies just released a new version (dependency version number update).
* you need an additional package for data analysis (add a new dependency).
* you have found a better package and no longer need the older package (add new dependency and remove old dependency).

If any of these occur, all you need to do is update the contents of your environment.yml file accordingly and then run the following command:

    $ conda env update --prefix ./env --file environment.yml
See: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#id3
