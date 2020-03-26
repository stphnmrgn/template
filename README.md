# template
Template repository that can be cloned and used to create a python environment and git repository for a project. It includes the following files to initiate a basic conda/git project.

- README
- conda environment .yml file
- license
- python gitignore

The yml file should be customized before creating a conda environment from step 5 below (i.e. update the yml file to include whatever python packages you need for reproducible projects *before* creating the python environment.

1. Clone this repo

       $ git clone https://github.com/stphnmrgn/template.git
   
2. Create a project folder

       $ mkdir new_project
       
4. Copy/paste the content from "template" into your project folder. Alternatively you could rename the "template" repo folder and use it as your project folder

5. Rename the conda environment in the first line of the yml file. The yml file is used to create a python environment, and so editing the name (first line), packages, and environment location (last line) in the yml file should be necessary every time you start a new project. The defaults environment name is template.
   
6. Finally, changed directories to your project folder, create the conda environment & activate it, and then create & push the repository to Github
    
    All together using `conda`:
    
       $ cd new_project
       $ conda env create
       $ source activate template
       $ git create
       $ git push -u origin master

Additionally, now that the inital environment is setup, we can use the same environment for multiple projects. We just need to copy and paste the yml file (with the path removed from the last line) into the parent project directory. Side note: the last line of the yml file can be used to specify the path location to create the python environment. It is removed in this template yml file.

    $ mkdir new_project
    $ cd new_project
    ... 
    copy/paste yml file
    ...
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
