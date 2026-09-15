---
title: Running and Quitting
teaching: 15
exercises: 0
---

<!-- 
Maintainance notes:
Note that the <kbd>x</kbd> tags are HTML keyboard tags for rendering text as keyboard buttons. 
-->



::::::::::::::::::::::::::::::::::::::: objectives

- Launch an integrated development environment (IDE)
- Create a new Python program.
- Understand the difference between a program and a code cell.
- Create and run a Python program.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- How can I run Python programs?

::::::::::::::::::::::::::::::::::::::::::::::::::

To run Python, we will be using an integrated development environment (IDE). An IDE
is a software program that combines commonly used development tools to provide a 
helpful environment for writing, editing, and running code. Examples of IDEs include
[Spyder][spyder], [PyCharm][pycharm], [Visual Studio Code][vs-code], and [JupyterLab][jupyterlab].
Developers also use text editors like Vim or Emacs, though they have less features. After editing
and saving your Python program you can execute those programs within the IDE itself or directly in the command
line.

For this workshop, we will be using **Spyder**. Spyder is a powerful and commonly used IDE
with many features that can help users to develop, test, and explore code. Spyder's features
include:

- You can easily type, edit, copy, and paste blocks of code. Spyder also allows you to easily add
  quotation marks, brackets, comment hashes, and indentation around blocks of code with a single click.
- Tab complete allows you to easily access the names of things you are using
  and learn more about then.
- The variable explorer allows you to explore and view the variables that have been created
  in a coding session.
- Hovering your cursor over a variable or function gives you more information on it.
- It allows you to display figures inside the code editor.
- You can create code blocks that operate like the cells used in Jupyter notebooks.
  These act like separate cells which can be run individually and in any order.
- Spyder Projects allow you to create and load separate sessions for each project which will
  remember their preferences and setups, easily allowing you to switch seamlessly between projects.


## Getting Started with Spyder

Spyder is a locally run program that is supported in Windows, MacOS, and Linux. Spyder is included as part of the 
Anaconda Python distribution, or can be installed by itself, and has a .
If you have not already installed the Anaconda Python distribution and Spyder, please see
[the setup instructions](../learners/setup.md) for installation instructions.

## Starting Spyder directly
To start Spyder, go to your computers application browser and select Spyder. This works regardless
of whether you installed it standalone or through Anaconda.
 
### Anaconda Navigator
To start Spyder from the Anaconda Navigator you must first 
[start Anaconda Navigator (click for detailed instructions on macOS, Windows, and Linux)][anaconda-start-nav]. 
You can search for Anaconda Navigator via Spotlight on macOS (<kbd>Command</kbd> + <kbd>spacebar</kbd>), 
the Windows search function (<kbd>Windows Logo Key</kbd>) or opening a terminal shell and 
executing the `anaconda-navigator` executable from the command line.

After you have launched Anaconda Navigator, click the `Launch` button under JupyterLab. You may need
to scroll down to find it.

Here is a screenshot of an Anaconda Navigator page similar to the one that should open on either macOS
or Windows.

<p align='center'>
  <img alt="Anaconda Navigator landing page" src="fig/0_anaconda_navigator_landing_spyder.png" width="750"/>
</p>


### Anaconda Prompt
To start Spyder from the command line using Anaconda Prompt, follow these steps:

- Launch Anaconda Prompt
  - [OPTIONAL]: If using a custom environment, activate it with `conda activate [environment_name]`
- Launch Spyder by entering the command `spyder`.

## The Spyder Interface

Spyder has many features designed to improve the coding and development experience, many of which
are shared across different integrated development environments (IDEs).

Upon opening, the Spyder interface consists of a top navigation bar and several different panes.
These panes include  the main editor pane, a multi-section tabbed pane consisting of the Help, 
Variable Explorer, Debugger, Plots, and Files panes, and an IPython console and History pane. Each of the panes can be resized
by clicking on the edge of the point and dragging. Likewise, panes can be detached and moved, hidden,
and new panes can be added.

### Menu Bar

The Menu Bar at the top of Spyder has the top-level menus that expose various actions
available in JupyterLab along with their keyboard shortcuts (where applicable). The following
menus are included by default.

- **File:** Actions related to files and directories such as *New*, *Open*, *Close*, *Save*, etc. 
The *File* menu also includes the *Exit* and *Restart* actions used to shutdown or restart Spyder,.
- **Edit:** Actions related to editing documents and other activities such as *Undo*, *Cut*, *Copy*, *Paste*, etc.
- **Search:** Enables a detailed search function across directories, projects, and files.
- **Source:** Enables actions relating to formatting and navigating the editor pane.
- **Run:** Actions for running code in different activities such as programs and code blocks.
- **Debug:** Actions relating to running code in debug mode, which is used to test code and find any issues.
- **Consoles:** Actions for managing code consoles. Consoles in Spyder will be explained in more detail below.
- **Projects:** Actions relating to creating, loading, and using Projects in Spyder.
- **Tools:** Actions relating to controlling the setting and behaviour of Spyder. Notably includes the *Preferences* section, which has the detailed Spyder settings.
- **View:** Actions that alter the appearance of Spyder.
- **Help:** Shows links and resources for getting help with Spyder, and how to report an issue.


### Editor pane

The editor pane is where you can write code into Python programs. It can contain multiple tabs,
each with its own program. At the top of the editor pane the path to the selected file is shown.
On the left, the line number for each line is shown. At the top right is an options button
which contains options for controlling editor tabs or navigating to specific lines. A vertical
line is also shown going down the editor pane; this shows the width of 80 characters,
which is a standard convention for suggested maximum line length in Python code..



<p align='center'><img alt="Spyder editor pane" src="fig/0_spyder_editor_pane.png"/></p>


:::::::::::::::::::::::::::::::::::::: instructor
### Directories and folders
You may need to explain the usage of the term 'directory' instead of 'folder' for some participants.
Folders and directories generally refer to the same thing, though the term directory is the more technical
term from command-line systems, and is the older term. 'Folder' was introduced as a visual term 
for graphical interfaces. Both terms generally refer to the same thing and can be used interchangeably, 
though it's best to be consistent. Do note though that some 'Folders' in systems like Windows are not directories,
but rather virtual objuects such as the Control Panel or Recycle Bin, and do not map to a directory on the drive.

:::::::::::::::::::::::::::::::::::::::::::::::::

### Files pane
The files pane is a filesystem and directory browser built into Spyder. You can use this pane to view and filter 
files by type and extension, open them directly into the editor, create or delete directories, set the working directory,
and perform many other common operations on files and directories.


### Help pane
The help pane is used to show help messages and information on any Python objects.
You can get help when coding by pressing <kdb>Ctrl</kbd> + <kbd>I</kbd> in front of it,
either in the Editor or in the Console.



### Variable explorer pane
The Variable Explorer pane shows the values, types, and size of any variables created in the current Python
session. This can include variables created from multiple different programs or directly in the console.

Double clicking on variables allows you to edit the value of the variable. If the variable is a data structure
like a list, dictionary, or dataframe, you can double click the variable value to open a new window where you can 
view and edit the values of the variable.

Variables edited in the variable explorer will not affect variables created in the editor, but can affect
variables called directly in the console. We will go into variables in more detail in the [next chapter](./02-run-quit.md).

<p align='center'><img alt="Spyder Variable Explorer" src="fig/0_spyder_variable_explorer.png"/></p>


### Debugger pane
The debugger pane allows you to view any issues or errors within your code, view the source codes
where issues have arisen, and control the workflow of debugging Python code.

### Plots pane
The plots pane is where any visualisations can be shown. If any plots are generated they can be viewed,
saved, or deleted in this pane.

By default, Spyder has the option *Mute inline plotting* active; meaning that any plots are shown in
the Plots pane. If turned off, plots can instead be shown in the active console, or shown in a separate 
window.

### IPython Console pane
The console pane (or IPython Console) allows you to execute code directly inside the Python interpreter.
Like the editor pane, the console pane can hold multiple tabs, each representing a different terminal.

<p align='center'><img alt="Spyder IPython console pane" src="fig/0_spyder_terminal.png"/></p>

:::::::::::::::::::::::::::::::::: callout
### Other panes

Spyder contains other panes which are not shown by default, but can be activated by going to
***View > Panes***, and clicking on the name of the pane. Notable examples include the 
*Outline pane* which allows you to navigate to sections within your code, the 
*Find pane* which holds a text search function, and the *Project pane* which holds
information about a current Spyder project, if one is active.
You can also use this section to hide currently shown panes.

:::::::::::::::::::::::::::::::::::::::::::



:::::::::::::::::::::::::::: instructor
The below spoiler is added to give some information on the Python kernels in the console.
In particular, it is added for instances where a participant's environment has issues and their
spyder-kernels installation cannot be found.

:::::::::::::::::::::::::::::::::::::::


:::::::::::::::::::::::::::::::::::::::::  spoiler

## Kernels and consoles

Spyder is able to run Python, including in separated code cells, by connecting to a kernel.
A kernel is a separate process that can run dirrerent programming languages and environments.
When opening Spyder, it should automatically connect to a Python kernel. If we wish, we can 
also connect to different Python kernels should we wish to run a different version of Python.

When we run code, it is run through the console, which connects to the kernel. We can either run code through
a program, or by entering it into the console directly. We can also delete and create new consoles,
open consoles in specific coding environments, or open consoles that have remote connections to
external servers.


Should you need to update or reinstall the kernels used by Spyder in a conda environment, use
the following commands in Anaconda prompt:
To install:
```bash
conda install conda-forge::spyder-kernels
```

To update:
```bash
conda update spyder-kernels
```
::::::::::::::::::::::::::::::::::::::::::::::::::



## Creating a Python program

When opening Spyder, a tab called temp.py will have been created. You can immediately start writing 
Python code there. Alternatively, to create a new Python program in a new tab, click **File > New File**, 
which will create a new tab.

You can also create a new file in the File Explorer pane by right clicking inside a directory, 
clicking *New File*, and selecting a Python file. Python files will have the `.py` extension; this lets 
everyone (including the operating system) know that this text file is a Pytho program.



##  Maths and strings

We can use the Python interpreter directly as a calculator. We can run code directly in the console,
or we can write it in the editor. 

For example:
```python
3 + 5
```

```output
8
```

Note that if we run this is the Spyder editor with the *Run File* option (Windows shortcut F5; Mac ), 
it will not display a value; however if we run it in the console, or with the *Run Cell* option (shortcuts 
<kbd>Ctrl</kbd> + <kbd>Enter</kbd> on Windows, or <kbd>Cmd</kbd> + <kbd>Enter</kbd> on Mac), it will 
show the result.


Likewise we can show text. Text values in Python must be written in quotation marks,
either single quotation marks (`''`), or double quotation marks (`""`).
For example
```python
"Hello world!"

```

```output
Hello world!
```



## Comments
An important part in writing good Python code is legibility. We want to be able to read our own or 
each other's code, and an important part of that is leaving comments.

A comment is a seciton of text in a Python program that is not run by the computer. We can write
a comment in Python by using the hash symbol (`#`). When we do so, anything after the `#` is treated
as a comment; it is not run by the computer. If put at the start of a line, the whole line will be a comment.
Likewise, we can put a comment partway through a line; only the code after the `#` will be treated as a comment.

A common convention is to also put a space after the `#`. This is not a Python requirement, but a 
convention to help make the code more readable.

For example:

```python
# This is a comment

1 + 3 * 8 # We can put a comment after other code
```

```output
25
```


We can also create longer comments that spread across multiple lines. There are two methods for this.
The first is to simply use multiple consecutive lines with `#` symbols. For example:
```python
# First line of a comment
# Second line of a comment
# Third line of a comment
```

Another method is to use text enclosed with three triple quotes (`'''` or `"""`). For example:

```python
"""
This is another way to create a long, multi-line comment.
It also has some other uses, and is commonly used
when documenting Python programs.
"""
```


::::::::::::::::::::::::::::::::::::: spoiler
### Multiline string literals as comments

Using text in enclosed triple quotes is a convenient way to create longer comments without
repeatedly uses hashes, though they are technically different to true comments.

The Python compiler does not ignore the enclosed text like it does with a true comment; it
instead passes it to memory but does not run it if it is not attached to a variable.
In some instances it can be be used as a docstring, which is used in documentation.

:::::::::::::::::::::::::::::::::::::::::::::




## Creating code cells
::::::::::::::::::::::::::::::: instructor
When running the workshop, it is best to be consistent regarding whether you regularly used code 
cells, or to run the Python programs directly.

::::::::::::::::::::::::::::::::::::::::::

In Spyder we can create and run code cells. A code cell is an isolated piece of code that can be run individually, regardless of its
place in the program, or can be run as part of the program as a whole.

We can define the start of a new code cell using the hash symbol followed by two percent symbols (`#%%`).
As the code cell starts with a hash, it also counts as a comment, and we can put other text after
it if we wish.

```python
#%% This is a code cell

1 + 3


# %% This also starts a code cell, and is the end of the previous cell

3 * 5

```


A code cell continues on until a new code cell is defined. You can have as many code cells as you like, or none at all.
Note that code cells are a feature used in Spyder (as well as some other IDEs); it is not a core Python function.

We can run the code in a code cell using the *Run Cell* button, or with the shortcuts 
<kbd>Ctrl</kbd> + <kbd>Enter</kbd> (Windows), or <kbd>Cmd</kbd> + <kbd>Enter</kbd> (Mac).



:::::::::::::::::::::::::::::::::::::::  challenge

## More Math

What is displayed when a Python code cell
that contains several calculations is executed?
For example, what happens when this cell is executed?

```python
7 * 3
2 + 1
```

:::::::::::::::  solution

## Solution

Python returns the output of the last calculation.

```python
3
```

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::






[spyder]: https://www.spyder-ide.org/
[vs-code]: https://code.visualstudio.com/
[jupyterlab]: https://jupyterlab.readthedocs.io/en/stable/
[jupyterlab-ui]: https://jupyterlab.readthedocs.io/en/stable/user/interface.html
[jupyterlab-overview]: https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html#overview
[jupyterlab-notebook-docs]: https://jupyterlab.readthedocs.io/en/stable/user/notebook.html
[markdown]: https://en.wikipedia.org/wiki/Markdown
[data_carpentry]: https://datacarpentry.org
[anaconda-start-nav]: https://docs.anaconda.com/free/navigator/getting-started/#navigator-starting-navigator
[pycharm]: https://www.jetbrains.com/pycharm/

:::::::::::::::::::::::::::::::::::::::: keypoints

- Python programs are plain text files.
- Use Spyder for editing and running Python.
- You can run maths or show text directly in the Python interpreter
- Spyder can optionally have code cells which can be run independently.



::::::::::::::::::::::::::::::::::::::::::::::::::


