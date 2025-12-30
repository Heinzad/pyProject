<!-- docs\about-main.md -->

Main Entry Point
================

This script provides an entry point to the project. It should be run as a script, not a module.

- A Python file run as a script serves as the main program to be executed. 

- When a file is run as a script, the special variable `__name__` is set to `"__main__"`.

### Example: 

*Python:* 

Write the code to be run as a script, not a module: 

```python
# main.py 

def main():
    pass

if __name__ == "__main__":

    main()
```

### Usage: 

*Command Line:*

```
python main.py
```