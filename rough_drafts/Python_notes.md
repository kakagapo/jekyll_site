curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
sudo python get-pip.py

sudo pip install --user pipenv -> also installs virtual env
sudo -H pip install virtualenv

To install PyGTK:
=================
sudo apt-get install python-gtk2

virtualenv commands:
====================

1. virtualenv --version
2. cd my_project_folder; virtualenv my_project
3. Use virtualenv -p /usr/bin/python2.7 my_project to use the specific version of python interpreter.
