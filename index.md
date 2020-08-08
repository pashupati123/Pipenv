## Development of Python Projects with Different Dependencies using pipenv


### pipenv Introduction
Pipenv is a packaging tool python which provide an isolated environment for the development of the python project without any interference of exiting or overriding with the installed packages of the other python project. 
It provides deterministic build by providing the production environment match those in the development environment exactly.
It consolidates and simplifies the development process to a single command line tool which very easy to use and handle.



### First, let’s install it

```markdown
pip install pipenv

```
### Spawn Shell in a Virtual environment
Create and open Python application.

```markdown
pipenv install —python <#python-version>
```
It  introduces two new files, the Pipfile (which is meant to replace requirements.txt) with the specific python version specified in command and the Pipfile.lock (which enables deterministic builds).


spawn a shell in a virtual environment to isolate the development of this app.
```markdown
pipenv shell
```
This will create a virtual environment if one doesn’t already exist.




### Install the 3rd party package for this app

```markdown
pipenv install <specific-package>
```
It will put the dependency in  [packages] location in the Pipfile.

```markdown
pipenv install <specific-package>  --dev
```
Providing the --dev argument will put the dependency in a special [dev-packages] location in the Pipfile, which will use dependency only for development eg: pytest - Python testing package.


### Run the app locally 
```markdown
pipenv run python <python-file-name>
```

### Ready To Push 
Okay, so let’s say you’ve got everything working in your local development environment and you’re ready to push it to production. To do that, you need to lock your environment so you can ensure you have the same one in production.
It enables deterministic builds by specifying the exact requirements for reproducing an environment. It contains exact versions for packages and hashes to support more secure verification.

```markdown
pipenv lock
```





