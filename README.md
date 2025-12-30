# pyProject

A Skeleton structure for python projects.


![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 

[![GitHub license](https://badgen.net/github/license/Naereen/Strapdown.js)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)



Project Structure
-----------------

The top level holds: 
- .env: environment variables (ignored by git)
- .gitignore: excludes filetypes from upload to git
- requirements: package dependencies

The directories are: 
- .venv : virtual environment (ignored by git)
- docs : documentation
- src : source code
- tests : test scripts 


```
.
├── .venv/
├── docs/
├── src/
|   ├── __init__.py
|   └── ...
├── tests/
├── .env
├── .gitignore
├── requirements.txt
└── ...

```




Requirements
------------

The following libraries are required: 

| name | description | 
| ------- | ----------- | 
| python-dotenv | Loads parameters from the .env file into environment variables. |



License
-------

This project uses the MIT license.
