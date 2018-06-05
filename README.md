# python_abcs
One step at a time into the world of python to dig deeper into Machine Learning and Artificial Intelligence

# installation
At the time of creating this project, the version of Python is 3.6.5 . I am using Mac as a development environment. Here are the steps to install Python and get it to run within your Mac environment.

If homebrew is not installed, install it from https://brew.sh/ .

## Install Python: `brew install python`

Make sure that brew has permission to modify /usr/local to create symlinks after installing Python. If you are not the administrator, the installation with fail at creating symlinks for your python. A successful installation will install python in your development environment, create symlinks to allow you run python REPL commands and runs post installation steps.

Once the installation is successful, run `python -V`. If this command is successful, you will see that the python is successfully installed and the version of the installed python is shown in your terminal.

As part of post installation steps, brew also installs `pip` a package manager used to manage python software packages. You can check if pip is installed or not using the command `pip --version`.

If you are into Software development, you might have had a dependency problem at some point of your experince. If not, then you are probably the luckiest developer of all times. In order to make sure that a version of software dependency package in one project doesnt effect the functionality of other, a project level dependency manager is very useful. Pipenv is one of those tools in python. Lets install pipenv.

## Install Pipenv: `pip install --user pipenv`

Pipenv is a higher level tool which simplifies the python dependency managemnt. `--user` in the command makes sure that the pipenv installation is at a user level.

### Add pipenv to you profile

Run `python -m site --user-base` to get the location of Python installation. Append `/bin` to the path of the python installation. This will provide the path at which pipenv is available. Now update $PATH with the path of pipenv to have it accessible in terminal. You can do this by adding `export PATH=$PATH:<python installation path>/bin` in your `~/.bash_profile` file.

### Add Pipfile to your project

Navigate to your project location. Once you are in the root location of your project run `pipenv install requests==2.18.4`. This command will create a virtualenv for your project and initializes a Pipfile in your project with 2.18.4 version of `requests` package. This file keeps track of all the dependencies required for your project and its version numbers. Check `https://docs.pipenv.org/` for further documentation of pipenv usage.
