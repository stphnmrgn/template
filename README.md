# template
Template repository that can be cloned within a project folder and used to create a python environment and git repository for that project. It includes the files (README, conda env yml, license, and python gitignore) to initiate a basic conda/git project. Items should be  be customized before step 3 below (i.e. update the yml file to include whatever python packages you need for reproducible projects *before* executing steps 3-5 below).

1. Clone this repo where ever you want your project to be located.
2. Rename the repo from `template ` to your project/feature name, and then edit the name within in the yml file to match your project name. 
    - The yml file is used to create a python environment, and so editing the name and packages in the yml file should be necessary every time you start a new project.
3. Fire up conda and change directory to the project directory using **$ cd C:\Users\Path\To\project_name**
4. Create conda environment with **$ conda env create**
5. Activate the conda environment with **$ source activate template**
6. To push the repository to Github, use Github’s hub command **$ git create** (or via GitHub's website UI), then push the master branch with **$ git push -u origin master**
