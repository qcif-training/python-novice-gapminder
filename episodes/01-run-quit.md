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

- **File:** Actions related to files and directories such as *New*, *Open*, *Close*, *Save*, etc. The *File* menu also includes the *Exit* and *Restart* actions used to shutdown or restart Spyder,.
- **Edit:** Actions related to editing documents and other activities such as *Undo*, *Cut*, *Copy*, *Paste*, etc.
- **Search**:
- **Source:**
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



<p align='center'>   <img alt="Spyder editor pane" src="fig/0_spyder_editor_pane.png" width="250"/></p>


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

<p align='center'>   <img alt="Spyder Variable Explorer" src="fig/0_spyder_variable_explorer.png" width="250"/></p>


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



:::::::::::::::::::::::::::::::::: callout
### Other panes

Spyder contains other panes which are not shown by default, but can be activated by going to
***View > Panes***, and clicking on the name of the pane. Notable examples include the 
*Outline pane* which allows you to navigate to sections within your code, the 
*Find pane* which holds a text search function, and the *Project pane* which holds
information about a current Spyder project, if one is active.
You can also use this section to hide currently shown panes.

:::::::::::::::::::::::::::::::::::::::::::




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
```
conda install conda-forge::spyder-kernels
```

To update:
```
conda update spyder-kernels
```
::::::::::::::::::::::::::::::::::::::::::::::::::



## Creating a Python program

To start writing a new Python program, 
- To start writing a new Python program click the Text File icon under the *Other* header in the Launcher tab of the Main Work Area.
  - You can also create a new plain text file by selecting the *New -> Text File* from the *File* menu in the Menu Bar.
- To convert this plain text file to a Python program, select the *Save File As* action from the *File* menu in the Menu Bar 
  and give your new text file a name that ends with the `.py` extension.
  - The `.py` extension lets everyone (including the operating system) know that this text file is a Python program.
  - This is convention, not a requirement.





## Creating code cells
In Spyder we can create and run code cells. A code cell is an isolated piece of code that can be run individually, regardless of its
place in the program, or can be run as part of the program as a whole.

We can define the start of a new code cell using the hash symbol (`#`) followed by two percent symbols (`%`), as below:

```python
#%%

```
A code cell continues on until a new code cell is defined. You can have as many code cells as you like, or none at all.

Note that code cells are a feature used in Spyder (as well as some other IDEs); it is not a core Python function.


## Creating a Jupyter Notebook

To open a new notebook click the Python 3 icon under the *Notebook* header in the Launcher tab in
the main work area. You can also create a new notebook by selecting *New -> Notebook* from the *File* menu in the Menu Bar.

Additional notes on Jupyter notebooks.

- Notebook files have the extension `.ipynb` to distinguish them from plain-text Python programs.
- Notebooks can be exported as Python scripts that can be run from the command line.

Below is a screenshot of a Jupyter notebook running inside JupyterLab. If you are interested in
more details, then see the [official notebook documentation][jupyterlab-notebook-docs].

<p align='center'>   <img alt="Example Jupyter Notebook" src="fig/0_jupyterlab_notebook_screenshot.png" width="750"/>
</p>







:::::::::::::::::::::::::::::::::::::::  challenge

## Arranging Documents into Panels of Tabs

In the JupyterLab Main Work Area you can arrange documents into panels of tabs. Here is an
example from the [official documentation][jupyterlab].

<p align='center'>   <img alt="Multi-panel JupyterLab" src="fig/0_multipanel_jupyterlab_screenshot.png" width="750"/>
</p>

First, create a text file, Python console, and terminal window and arrange them into three
panels in the main work area. Next, create a notebook, terminal window, and text file and
arrange them into three panels in the main work area. Finally, create your own combination of
panels and tabs. What combination of panels and tabs do you think will be most useful for your
workflow?

:::::::::::::::  solution

## Solution

After creating the necessary tabs, you can drag one of the tabs to the center of a panel to
move the tab to the panel; next you can subdivide a tab panel by dragging a tab to the left,
right, top, or bottom of the panel.



:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::



## The Notebook has Command and Edit modes.

- If you press <kbd>Esc</kbd> and <kbd>Return</kbd> alternately, the outer border of your code cell will change from gray to blue.
- These are the **Command** (gray) and **Edit** (blue) modes of your notebook.
- Command mode allows you to edit notebook-level features, and Edit mode changes the content of cells.
- When in Command mode (esc/gray),
  - The <kbd>b</kbd> key will make a new cell below the currently selected cell.
  - The <kbd>a</kbd> key will make one above.
  - The <kbd>x</kbd> key will delete the current cell.
  - The <kbd>z</kbd> key will undo your last cell operation (which could be a deletion, creation, etc).
- All actions can be done using the menus, but there are lots of keyboard shortcuts to speed things up.



:::::::::::::::::::::::::::::::::::::::  challenge

## More Math

What is displayed when a Python cell in a notebook
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
- The Notebook has Command and Edit modes.
- Use the keyboard and mouse to select and edit cells.
- The Notebook will turn Markdown into pretty-printed documentation.
- Markdown does most of what HTML does.

::::::::::::::::::::::::::::::::::::::::::::::::::


