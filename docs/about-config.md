<!-- docs\config.md -->



config: Application Configurations
==================================

Centralise environment variables as parameters in a top-level file that acts as a single source of truth that lower-level scripts can access. 
- Help developers avoid the temptation of hardcoding secrets. 
- Define where configuration values come from and which source wins if there is a conflict.


(1) Import Package Dependencies
-------------------------------

The `os` module is part of Python's standard library and provides access to operating system features. The `dotenv` module reads the contents of the `.env` file and loads them into environmental variables. 


Pseudocode: 

1. Import all of `os`, the operating system interface module, so that I can use its commands. 
2. Import the `load_dotenv` function only from the `dotenv` package. 
3. load variables from the `.env` file into environment variables with the `load_dotenv` function. 


```python
    import os
    from dotenv import load_dotenv 
    load_dotenv()
```

(2) Parameterise the Environment Variables
------------------------------------------

Access configuration values without hardcoding them.

Pseudocode: 

1. Initialise the PARAMETER 
2. giving the matching VARIABLE name to 
2. the `os.getenv()` function.

Apply this python syntax for the parameter to be made available to the entire application: 

```
    PARAMETER = os.getenv('VARIABLE')
```
