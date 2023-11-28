# Create a Python program

The configuration files used for Black, Flake8, Pylint, and Pytest are as follows:

- Black: Black only supports the TOML file format for its configuration, which should be placed in the root of your project. Compatible configuration files for other tools can be found in the provided examples

- Flake8: Flake8 can be configured using various configuration files, such as .flake8, setup.cfg, and tox.ini. Flake8 should be configured to allow lines up to the length limit of 88, Black’s default

- Pylint: Pylint can be configured using configuration files such as pylintrc and setup.cfg. Pylint should be configured to only complain about lines that surpass 88 characters via max-line-length = 88. If using pylint<2.6.0, also disable C0326 and C0330 as these are incompatible with Black formatting and have since been removed

- Pytest: Pytest can be configured using a configuration file named pytest.ini. Other configuration files such as setup.cfg and tox.ini can also be used to hold pytest configuration if they have a [tool:pytest] section

It is important to note that some of these tools may need a bit of tweaking to resolve conflicts, and there are other popular Python linters and formatters besides the ones mentioned here
