.. -*- coding: utf-8 -*-

.. role:: raw-html(raw)
   :format: html

Using Specter
##################

Installation
=============
You can download Specter from PyPI for easy installation.
It is recommended that you use  `pip
<http://pypi.python.org/pypi/pip>`_ or `easy_install
<http://python-distribute.org/distribute_setup.py>`_ to install the bindings::

  pip install specter

You may consider using `virtualenv <http://www.virtualenv.org>`_ or `pyenv <https://github.com/yyuu/pyenv>`_ to create isolated Python environments.

Setup
==========
By default, Specter looks within the current directory for a folder called "spec" which contains your test files

*Example Default Test Structure:*

::

   Project_Folder
       └── spec
           ├── submodule
               ├── another.py
               └── __init__.py
           ├── example.py
           └── __init__.py

If you do not which to use the default folder, you can specific an alternative using the :raw-html:`"--search"` command-line argument::

   specter --search /path/to/folder

Runner
==============
Specter allows for quick and easy execution of your tests by just calling 'specter' within your project folder::

	specter
	          ___
	        _/ @@\
	    ~- ( \  O/__     Specter
	    ~-  \    \__)   ~~~~~~~~~~
	    ~-  /     \     Keeping the Bogeyman away from your code!
	    ~- /      _\
	       ~~~~~~~~~

	ExampleSpec
	  ∟ this is a test spec


	------------------------
	------- Summary --------
	Pass            | 1
	Skip            | 0
	Fail            | 0
	Error           | 0
	Incomplete      | 0
	Test Total      | 1
	 - Expectations | 1

	------------------------

Command-line Arguments
------------------------
Specter is a spec-based testing library to help facilitate BDD in Python.

=====================  ============
Argument               Description
=====================  ============
-h, --help             Show console help
--search PATH          Specifies the search path for spec files
--no-art               Disables the ASCII art on the runner
--coverage             Enables coverage.py integration. Configure using .coveragerc
--select-module        Selects a module path to run. Ex: sample.TestClass
--select-tests         Selects tests to run by name. (Comma delimited list)
--select-by-metadata   Selects tests to run by specifying a list of key=value pairs
--xunit-results        Output xUnit XML results into a specified file
--json-results         Saves Specter JSON results into a specifed file
--no-color             Disables ASCII color codes
--ascii-only           Disables color and uses only ascii characters (useful for CI systems).
--parallel             Activates parallel testing mode
--num-processes        Specifies the number of processes to use under parallel mode (default: 6)
--show-all-expects     Displays all expectations for test cases
=====================  ============
