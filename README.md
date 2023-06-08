# django_project-

●	Initialise a local Git repo for the project.
●	If your Django project doesn’t have a requirements.txt file, please create it before proceeding.

pip install -r requirements.txt
All the packages listed in the requirements.txt file will be installed at once.
The requirements.txt file can be created manually, but there is a simple command to auto-generate this file. Navigate to your root directory with	your	virtual	environment	activated	and	run	the	following command:
python -m pip freeze -l > requirements.txt
(Please note that on some systems, you may have to use pip3 instead of 

●	Commit the project to the local repo.
●	Branch from the master/main branch and name the new branch ‘docs’
●	In the ‘docs’ branch, add docstrings for a few of your functions, classes and modules/scripts. You can keep the documentation concise.
○ Commit the changes for each documented script one at a time before proceeding with the documentation of the next script. This ensures that you can rollback any changes you would have made should you need to.

●	Generate user-friendly documentation using Sphinx and ensure you have the output stored in a docs folder in the project directory. For example:
○ hyperion/
■ blog/
■ docs/
■ hyperion/
■ polls/
■ …

When setting up Sphinx for Django projects you will need to add the following to your conf.py file:
import os
import sys
import django
sys.path.insert(0, os.path.abspath('..'))
os.environ['DJANGO_SETTINGS_MODULE'] = 'Your_project_name.settings'
django.setup()

created a new app in your Django project (e.g. ‘blog.settings’)
Please do not exclude the generated documentation for this project because you want the audience of your repo to have easier access to your documentation. If you wish, you can investigate using pre-commit Git hooks to automate this, but note that this is not required.
●	Commit all changes to the docs branch.
●	Switch to the master/main branch.
●	Branch from the master/main branch and name the new branch
‘container’
●	Add and commit a working Dockerfile to the container branch. Please ensure that your Django app works on a different computer.
●	Switch back to the master/main branch.
●	Merge the docs and container branches into the master/main branch.

■ Remember: you use a .gitignore file to ensure that sensitive files are not tracked by Git. Include the .gitignore file provided or, if you wish, create a .gitignore file and include the following code text inside of it and place this file file at the root of your Django project.
○ If it doesn’t already, please ensure that your repo includes a file named requirements.txt to automate the installation of the project’s requirements.
○ Remember to exclude any venv or virtualenv files from your repo.
