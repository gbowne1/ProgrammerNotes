# Create a Python program

In Python, a program usually starts with importing python libraries with `include`

The configuration files used for Black, Flake8, Pylint, and Pytest are as follows:

- Black: Black only supports the TOML file format for its configuration, which should be placed in the root of your project. Compatible configuration files for other tools can be found in the provided examples

- Flake8: Flake8 can be configured using various configuration files, such as .flake8, setup.cfg, and tox.ini. Flake8 should be configured to allow lines up to the length limit of 88, Black’s default

- Pylint: Pylint can be configured using configuration files such as pylintrc and setup.cfg. Pylint should be configured to only complain about lines that surpass 88 characters via max-line-length = 88. If using pylint<2.6.0, also disable C0326 and C0330 as these are incompatible with Black formatting and have since been removed

- Pytest: Pytest can be configured using a configuration file named pytest.ini. Other configuration files such as setup.cfg and tox.ini can also be used to hold pytest configuration if they have a [tool:pytest] section

It is important to note that some of these tools may need a bit of tweaking to resolve conflicts, and there are other popular Python linters and formatters besides the ones mentioned here

## A python Hello World

Here is a basic Python 3 Hello World

   ```py
   print("Hello, World!")
   ```

## Python program structure

From top to bottom, a typical Python program will have;

a shebang line #!/usr/bin/env python  This is optional.  It is only required if you plan to execute the script directly from the command line.

next if you are documenting the program, using `#` to comment and document the program

After the shebang line, one imports Python modules with `import`

Next, global variables are defined as in something like `GLOBAL_VARIABLE = "This is a global variable"`

After global variables next comes the function definitions using a `def`

If you are using OOP, next you would do some class definitions with `class`

last would be a main execution block with `if __name__ == "__main__":`
