<!-- docs\about-setup.md -->

setup
=====

The `setup` function in the `setuptools` package provides information for pip to install and manage Python packages for the project.


Parameters
----------

name : string  
    The name of the package. 

version : string  
    The version number of the package.

description : string   
    The description of the package.

author : string  
    The name of the author of the package. 

author_email : string   
    Email address of the author of the package.

packages : list   
    Names of the packages to be included in the distribution.

install_requires : list  
    Names of the package dependencies needing to be installed.

Example
-------

*Python:*  

#### Load the function from the library:  

```python
from setuptools import setup
```

#### Execute the function with parameters:

```python
setup(
    name='the_package',
    version='0.1',
    description='About the package',
    author='Author Name',
    author_email='author.name@example.com',
    packages=['the_package'],
    install_requires=[
        'python-dotenv',
    ],
)
```


Usage
-----

*Command Line:*  

#### Install the required library: 

```
pip install setuptools
```

#### Build and distribute the package: 

```
python setup.py sdist bdist_wheel
```

sdist :  
create a source distribution package containing the source code for the package. 

bdist_wheel :  
create a binary distribution package containing pre-compiled versions of the package's modules, which can be installed more quickly than a source distribution.


#### Install the package:

```
pip install the_package
```

#### Use the package:

*Python:*

```python
import the_package 
```

Summary
-------

`setup` contains the necessary information for building and distributing Python packages. 
  
  
Further Reading
---------------

- Geeks For Geeks (28 Apr 2025). [What is setup.py in Python?](https://www.geeksforgeeks.org/python/what-is-setup-py-in-python/).

- Joshua Phuong Le (3 Feb 2023). [Guide to Python Project Structure and Packaging](https://plainenglish.io/blog/a-practical-guide-to-python-project-structure-and-packaging)

