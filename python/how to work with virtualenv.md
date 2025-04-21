START
Basic
Front: 
How to work with `virtualenv`? What does it do? Which phases does it have? How does it discover the system python, and how to override it? What are the creators, seeders and activators?
Back: 
Create a virtual environment in current directory:
```sh
virtualenv venv
```

On Linux/Mac, activate it:
```sh
source venv/bin/activate
```

On Windows:
```sh
.\venv\Scripts\activate
```

To deactivate:
```sh
deactivate
```

The command `virtualenv venv` will create a python virtual environment in the `venv` directory, the python in this directory will be effectively isolated from the python that was used to create it.

It works in 2 phases:
1. Discover a python interpreter to create a virtual environment from (by default — the same version as the `virtualenv` itself is running from, can be changed by the `-p` option);
2. Create a python virtual environment at the specified destination:
	1. Create a python matching the target one;
	2. Install seed packages (one or more of `pip`, `setuptools`, `wheel`);
	3. Install activation scripts into the `bin` directory of the virtual environment;
	4. Create files that mark this directory to be ignored by VCS (only git is supported).

The created python environment is not self-contained (since it's not efficient to install python in the new folder), it's just a shell that borrows most from the system python, so upgrading the system python might break the virtual environment.

To override the default python version, use the `-p`/`--python` key with `{impl name}{version}{architecture}`, e.g., `python3.8.1-32`, `cpython3-64`, `pypy2`, or by specifying a path to the interpreter. The closest python to the specified version is discovered via registry (on Windows) or by going through the executables available in the `PATH` environment variable. 

`virtualenv` is configurable by creators, seeders and activators:
- **Creator** sets up the virtual environment. It's selected by the `--creator` argument, can either be the `venv` module from python installation (means running a new python process, unless `virtualenv` is installed in the system installation) or `builtin` which uses one of the built-in creators for various target environments, they know what files to create and which to reference.
- **Seeder** installs some seed packages (one or more of `pip`, `setuptools` and `wheel`); `setuptools` and `wheel` are disabled by default in Python 3.12+. Seeder is selected by the `--seeder` argument and is `app-data` by default, which means it will use the user application data directory to create images and link/copy them to the `site-packages` directory of virtual environment, so subsequent installations will be faster. Alternative is `pip` seeder which uses bundled `pip` to install seed packages from scratch to every virtual environment.
- **Activators** are scripts for different shells in the binary directory that mangle with shell settings (e.g., prepend `PATH` variable with the binary directory) to make sure the virtual environment executables take precedence over system ones. The `--activators` argument controls which scripts to generate, e.g., `bash`.

[User Guide - virtualenv](https://virtualenv.pypa.io/en/latest/user_guide.html)
<!--ID: 1745138811258-->
END
