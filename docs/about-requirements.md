<!-- docs\about-requirements.md -->



requirements: Python Library and Package Dependencies
=====================================================

Requirements are a list of the packages and their dependencies. The current list may be found in the `requirements.txt` file. 

- These instructions assume that packages are installed into the project's virtual environment directory `(.venv)`. 
- Instructions on using the virtual environment may be found in `docs\venv.md`. 


### Overview: 

1. Install a single package
2. Uninstall a single package
3. Save a list of packages
4. Install a list of packages
5. Uninstall a list of packages


Install a single package
------------------------


* Verify that the command prompt in the terminal is displaying the `(.venv)` directory path! 
* Use the `-m` module flag to force the use of this environments' python package installer only. 

Install a package to the virtual environment using the python package installer: 


*Bash terminal:*

```bash
    python -m pip install python-dotenv
```

Uninstall a single package
--------------------------

*Bash terminal:*

```bash
    python -m pip uninstall python-dotenv
```



Save a List of Installed Packages
---------------------------------


Pseudocode: 

1. Using the `python` language, 
2. With the `-m` flag to run the module like a script, 
3. Save to file using the `freeze` command, 
4. Redirecting (`>`) the output to 
5. the location where the `requirements.txt` file should be stored.  


*Bash terminal:*

```bash
    python -m pip freeze > requirements.txt
```

This will list the package and its version, as well as any dependencies that were automatically installed with the package. 


*Inspect the file contents:*

> python-dotenv==1.2.1  


Install a list of Required Packages
-----------------------------------

Pseudocode: 

1. Using the `python` language, 
2. With the `-m` flag to run the module like a script in this environment,
3. Perform the `install` operation, 
4. Reading (`-r`) the `requirements.txt` file that contains the list of packages to install.

*Bash terminal:*

```bash
    python -m pip install -r requirements.txt
```


Uninstall a List of Required Packages
-------------------------------------

Pseudocode: 

1. Using the `python` language, 
2. With the `-m` flag to run the module like a script in this environment,
3. Perform the `uninstall` operation, 
4. Reading (`-r`) the `requirements.txt` file that contains the list of packages to install,
5. Bypassing interactive prompts to state upfront that yes (`-y`) we do want to go ahead with this operation.


*Bash terminal:*

```bash
    python -m pip uninstall -r requirements.txt -y
```
