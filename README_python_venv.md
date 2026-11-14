# Virtual environments
A virtual environment is created on top of an existing Python installation, known as the virtual environment’s “base” Python, and by default is isolated from the packages in the base environment, so that **only** those **explicitly installed** in the **virtual environment** are available. 

## Creating virtual environments

Virtual environments are created by executing the venv module:

```python -m venv /path/to/new/virtual/environment```

## How venvs work
When a Python interpreter is running from a virtual environment, sys.prefix and sys.exec_prefix point to the directories of the virtual environment, whereas sys.base_prefix and sys.base_exec_prefix point to those of the base Python used to create the environment. It is sufficient to check sys.prefix != sys.base_prefix to determine if the current interpreter is running from a virtual environment.

### Activating the venv
A virtual environment may be “activated” using a script in its binary directory (bin on POSIX; Scripts on Windows). This will prepend that directory to your PATH, so that running python will invoke the environment’s Python interpreter and you can run installed scripts without having to use their full path. The invocation of the activation script is platform-specific (<venv> must be replaced by the path to the directory containing the virtual environment):

```source <venv>/bin/activate```

----
For details, further information and the bleeding edge on virtual environments see: https://docs.python.org/3/library/venv.html
