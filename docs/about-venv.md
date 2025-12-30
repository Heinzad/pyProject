<!-- docs\venv.md --> 

About the Virtual Environment
=============================

`venv` is the virtual environment where project dependencies are installed.

The following instructions describe using a virtual environment with Visual Studio Code (VS code).

- Installing packages in the virtual environment is described separately in `docs\about-requirements.md`. 

Using a project-specific virtual environment (rather than our machine's environment), isolates dependencies, preventing package versioning conflicts between projects. 

The virtual environment needs to be installed and activated before library packages are added to it. Once activated, its name will appear at the start of the command line in the terminal. 

Installing library packages may require administrator privileges. Once installed, they can be run in the virtual environment without elevated privileges. 



(0) PowerShell Preliminaries
----------------------------

If using Windows PowerShell, permit it to execute processes by removing restrictions on executing commands at the process scope: 

*PowerShell terminal:*

```powershell
Set-ExecutionPolicy Unrestricted -Scope Process
```


(1) Enable the Virtual Environment
----------------------------------

Administrative privileges are required to set up the virtual environment. 

(The following command is the same for both Git Bash and Windows PowerShell).  

With: 

1. `python` as the the language of this project, 
2. `-m` as the flag to run a module (rather than a script), 
3. `venv` as the virtual environment module in the Python standard library, 
4. `.venv` as the directory (listed in the .gitignore file) where the new environment will be installed; 

Use Git Bash to run the command: 

*Bash terminal:*

```bash
python -m venv .venv
```

We now have a virtual environment for the project, containing `pip` , its own Python package installer. We need to activate the virtual environment before we can use it. 


(2) Activate the Virtual Environment
------------------------------------ 

If using a large project with multiple virtual environments, use absolute paths to enable a specific virtual environment. If there is only one virtual environment, just use relative paths. 

If using Git Bash, provide the path to the activation script in the virtual environment directory we installed (above), using the `source` keyword: 

*Bash terminal:*

```bash
source .venv/Scripts/activate
```

If using Windows PowerShell, provide the path to the activation script for PowerShell, in the 'Scripts' directory of the virtual environment:  

*PowerShell terminal:*

```powershell
.venv\Scripts\Activate.ps1
```

If successful, command prompts will now be prefixed with `(.venv)`, the virtual environment directory. 


(3) Upgrade the Virtual Environment
-----------------------------------

* Verify that the command prompt in the terminal is displaying the `(.venv)` directory path! 
* Use the `-m` module flag to force the use of this environments' python package installer only. 
  
Upgrade to the latest version of this python package installer:

*Bash terminal:*

```bash
python -m pip install --upgrade pip
```




### (5) Deactivate When Finished 

You can stop the virtual environment running with the `deactivate` command:  

*Bash terminal:*

```bash
deactivate
```


