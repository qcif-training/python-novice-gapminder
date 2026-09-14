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
- Create a new Python script.
- Understand the difference between a script and a code cell.
- Create and run a Python script.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- How can I run Python programs?

::::::::::::::::::::::::::::::::::::::::::::::::::

To run Python, we will be using an integrated development environment (IDE). An IDE
is a software program that combines commonly used development tools to provide a 
helpful environment for writing, editing, and running code. Examples of IDEs include
[Spyder][spyder], [PyCharm][pycharm], [Visual Studio Code][vs-code], and [JupyterLab][jupyterlab].
Developers also use text editors like Vim or Emacs, though they have less features. After editing
and saving your Python scripts you can execute those scripts within the IDE itself or directly in the command
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
Variable Explorer, Debugger, Plots, and Files panes, and a console pane.

The [JupyterLab Interface][jupyterlab-ui]
consists of the Menu Bar, a collapsable Left Side Bar, and the Main Work Area which contains tabs
of documents and activities.

### Menu Bar

The Menu Bar at the top of Spyder has the top-level menus that expose various actions
available in JupyterLab along with their keyboard shortcuts (where applicable). The following
menus are included by default.

- **File:** Actions related to files and directories such as *New*, *Open*, *Close*, *Save*, etc. The *File* menu also includes the *Exit* and *Restart* actions used to shutdown or restart Spyder,.
- **Edit:** Actions related to editing documents and other activities such as *Undo*, *Cut*, *Copy*, *Paste*, etc.
- **Search**:
- **Source:**
- **Run:** Actions for running code in different activities such as scripts and code blocks.
- **Debug:** Actions relating to running code in debug mode, which is used to test code and find any issues.
- **Consoles:** Actions for managing code consoles. Consoles in Spyder will be explained in more detail below.
- **Projects:** Actions relating to creating, loading, and using Projects in Spyder.
- **Tools:** Actions relating to controlling the setting and behaviour of Spyder. Notably includes the *Preferences* section, which has the detailed Spyder settings.
- **View:** Actions that alter the appearance of Spyder.
- **Help:** Shows links and resources for getting help with Spyder, and how to report an issue.

:::::::::::::::::::::::::::::::::::::::::  callout

## Kernels and consoles

Spyder is able to run Python, including in separated code cells, by connecting to a kernel.
A kernel is a separate process that can run dirrerent programming languages and environments.
When opening Spyder, it should automatically connect to a Python kernel. If we wish, we can 
also connect to different Python kernels should we wish to run a different version of Python.

When we run code, it is run through the console, which connects to the kernel. We can either run code through
a script, or by entering it into the console directly. We can also delete and create new consoles,
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

A screenshot of the default Menu Bar is provided below.

<p align='center'>   <img alt="JupyterLab Menu Bar" src="fig/0_jupyterlab_menu_bar.png" width="750"/>
</p>

### Left Sidebar

The left sidebar contains a number of commonly used tabs, such as a file browser (showing the
contents of the directory where the JupyterLab server was launched), a list of running kernels
and terminals, the command palette, and a list of open tabs in the main work area. A screenshot of
the default Left Side Bar is provided below.

<p align='center'>   <img alt="JupyterLab Left Side Bar" src="fig/0_jupyterlab_left_side_bar.png" width="250"/>
</p>

The left sidebar can be collapsed or expanded by selecting "Show Left Sidebar" in the View menu or
by clicking on the active sidebar tab.

### Main Work Area

The main work area in JupyterLab enables you to arrange documents (notebooks, text files, etc.)
and other activities (terminals, code consoles, etc.) into panels of tabs that can be resized or
subdivided. A screenshot of the default Main Work Area is provided below.

If you do not see the Launcher tab, click the blue plus sign under the "File" and "Edit" menus and it will appear.

<p align='center'>   <img alt="JupyterLab Main Work Area" src="fig/0_jupyterlab_main_work_area.png" width="750"/>
</p>

Drag a tab to the center of a tab panel to move the tab to the panel. Subdivide a tab panel by
dragging a tab to the left, right, top, or bottom of the panel. The work area has a single current
activity. The tab for the current activity is marked with a colored top border (blue by default).

## Creating a Python script

- To start writing a new Python program click the Text File icon under the *Other* header in the Launcher tab of the Main Work Area.
  - You can also create a new plain text file by selecting the *New -> Text File* from the *File* menu in the Menu Bar.
- To convert this plain text file to a Python program, select the *Save File As* action from the *File* menu in the Menu Bar and give your new text file a name that ends with the `.py` extension.
  - The `.py` extension lets everyone (including the operating system) know that this text file is a Python program.
  - This is convention, not a requirement.

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



## Closing JupyterLab

- From the Menu Bar select the "File" menu and then choose "Shut Down" at the bottom of the dropdown menu. You will be prompted to confirm that you wish to shutdown the JupyterLab server (don't forget to save your work!). Click "Shut Down" to shutdown the JupyterLab server.
- To restart the JupyterLab server you will need to re-run the following command from a shell.

```
$ jupyter lab
```




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

- Python scripts are plain text files.
- Use Spyder for editing and running Python.
- The Notebook has Command and Edit modes.
- Use the keyboard and mouse to select and edit cells.
- The Notebook will turn Markdown into pretty-printed documentation.
- Markdown does most of what HTML does.

::::::::::::::::::::::::::::::::::::::::::::::::::


