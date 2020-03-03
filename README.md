# template
Template repository that can be cloned within a project folder and used to create a python environment and git repository for that project. It includes the initial files (README, conda env yml, license, and python gitignore) that can be customized before executing any processes (i.e. update the yml file to include whatever python packages you need for reproducible projects *before* steps 2-5 below).

1. Clone this repo
2. Fire up conda and change directory to the above repo using **$ cd C:\Users\Path\To\Repos\template**
3. Create conda environment with **$ conda env create**
4. Activate the conda environment with **$ source activate template**
5. To push the repository to Github, use **$ git create** using Github’s hub commands (or via GitHub's website UI), then push the master branch with **$ git push -u origin master**
