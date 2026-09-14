---
title: Setup
---

This lesson is an introduction to programming in Python 3 for people with little or no previous programming experience. 
It is based on the Carpentries' [Plotting and Programming for Python](https://swcarpentry.github.io/python-novice-gapminder)
workshop design, which is designed to be used in both Data Carpentry and Software Carpentry workshops.
This workshop references [Spyder](spyder) but can be taught using alternative Python 3 interpreters as well (e.g., repl.it, JupyterLab).

Setup for this workshop involves two steps: downloading the data, and installing Spyder.
Spyder can either be [installed directly](spyder-standalone), or installed through with the
[Anaconda Distribution](anaconda-install). Both methods for installation are detailed below; alternatively see the 
help pages for [installing Spyder](spyder-standalone) or [installing Anaconda](anaconda-install).



## Getting the Data

The data we will be using is taken from the [gapminder] dataset.
To obtain it, download and unzip the file
[python-novice-gapminder-data.zip](files/python-novice-gapminder-data.zip).



## Installing Spyder directly
Spyder can be installed directly on your computer without Anaconda. Installing Spyder in this methods comes with its own coding environment
with several core Python packages installed. The steps for installing Spyder are below, and can also be found at
the [Spyder installation guide](spyder-standalone).

- Seelct the installer for your computer's operating system
- Double click the installer file to open the installer on Windows or Mac OS
    - On Linux systems, use the bash command `bash path/to/downloaded/Spyder-Linux-x86_64.sh`
- If a security warning pops up, you may need to click `Yes`, `OK`, `Open`, or `Allow`, or on Windoes, `More Info` followed by `Run Anyway`.



## Installing Python and Spyder Using Anaconda
For this workshop, we will use [Spyder](spyder) as an integrated development environment (IDE), which we will install using the Anaconda Python Distribution.
We have the installation steps provided here, but please check the [Spyder installation Guide](spyder-install) or the
[Anaconda installation guide](anaconda-install) if you have any issues.
Installing the Anaconda Distribution will automatically install Spyder on your computer, along with Python and Jupyter Notebook.

First, we need to install Anaconda, which has installation steps for Windows, MacOS, and Linux.
The steps for installing the Anaconda distribution is found below for each operating system:


:::::::::::::::::::::::::::::::::::spoiler
### Installing Anaconda on Windows

- Navigate to the [Anaconda download page](https://www.anaconda.com/download).
- Select your operating system.
- Select the 64-Bit Graphical Installer under Anaconda Distribution. Each operating system has its own version.
- Once it has finished downloading, click the installer file to launch.
- Select **Next** and then **I Agree** to agree to Anaconda's [Terms of Service](anaconda-tos).
- Select an installation option:
    - **Just Me (Recommended)**: This installs only for the current user account. You can use this to install Anaconda on 
    an institutional device without administrator privileges.
    - **All Users**: This will install for all user accounts on the device. This will require administrator privileges.
- Press **Next**.
- Select a destination folder to install Anaconda in, then select **Next**.
- Select any optional installation settings:
    - Register Anaconda as my default Python installation: This registers the Python package in this install as the default
    Python installation for programs like VSCode, PyCharm, and Spyder.
    - Create Shortcuts: Selected by default. Creates Start Menu shortcuts for Anaconda Navigator, Spyder, Jupyter Notebook, and Anaconda Prompt packages.
- Select **Install**.
- Select **Next** twice, then select **Finish** to close the installer.


:::::::::::::::::::::::::::::::::::::::::::



:::::::::::::::::::::::::::::::::::spoiler
### Installing Anaconda on Mac OS
- Navigate to the [Anaconda download page](https://www.anaconda.com/download).
- Select your operating system.
- Select the 64-Bit Graphical Installer under Anaconda Distribution. Each operating system has its own version.
- Once it has finished downloading, click the installer file to launch.
- Select **Next** and then **I Agree** to agree to Anaconda's [Terms of Service](anaconda-tos).
- Select an installation option:
    - **Install for all users on this computer**: Installs Anaconda Distribution into `/opt/anaconda3` for all users fo the computer.
    - **Install on a specific disk**: Choose a different location in which to isntall the Anaconda Distribution.
- Press **Install**.

:::::::::::::::::::::::::::::::::::::::::::


:::::::::::::::::::::::::::::::::::spoiler
### Installing Anaconda on Linux
Use the following steps to install Anaconda on your Linux distribution. Many steps have alternate links or commands
depending on your Linux architecture (Linux x86 or AWS Graviton2/ARM64); please ensure you know which architecture
your computer has.

- Open your Linux terminal.
- Download the latest version of Anaconda Distribution and run one of the following commands:
    - curl (Linux x86): `curl -O https://repo.anaconda.com/archive/Anaconda3-2026.07-1-Linux-x86_64.sh`
    - curl (AWS Graiviton2/ARM64): `curl -O https://repo.anaconda.com/archive/Anaconda3-2026.07-1-Linux-aarch64.sh`
    - wget (Linux x86): `wget https://repo.anaconda.com/archive/Anaconda3-2026.07-1-Linux-x86_64.sh`
    - wget (AWS Graviton2/ARM64): `wget https://repo.anaconda.com/archive/Anaconda3-2026.07-1-Linux-x86_64.sh`
- Install the Anaconda distribution by running the appropriate command:
    - Linux x86: bash ~/Anaconda3-2026.07-1-Linux-x86_64.sh
    - AWS Graviton2/ARM64: bash ~/Anaconda3-2026.07-1-Linux-aarch64.sh
- Press <kbd>Return</kbd> to continue.
- Enter `yes` to agree to the Anaconda [Terms of Service](anaconda-tos).
- Pess <kbd>Return</kbd> to accept the default install location, or enter another file path.
- Choose `yes` when asked if you want to initialise conda. 
- Close and re-open your terminal window for the installation to fully take affect.
:::::::::::::::::::::::::::::::::::::::::::

After these steps, the Anaconda Distribution will be installed, with Spyder automatically installed as well. Spyder's installation
can be found in Anaconda's `(base)` environment. This is enough to run the Python packages needed for this workshop. 


### [OPTIONAL]: Setting up an Anaconda environment with Python packages
You can additionally create a new Anaconda environment from where you can install specific packages. To do so, follow these steps:

- Open Anaconda prompt
- Enter this command to create a new Conda environment: `conda create -c conda-forge -n spyder-env spyder numpy scipy pandas matplotlib`
    - This creates an environment with the following packages installed: Spyder (to run the IDE), Pandas, Numpy, Scipy, and MatPlotLib.
- Enter `y` to accept the environment installation.
- Once installed, enter the command `conda activate spyder-env` to activate the environment.
- If you wish to install any other packages, use the command `conda install [packagename]`.
- Once finished, you can exit the environment by closing the Anaconda prompt, or by using the command `conda deactivate`.







[gapminder]: https://en.wikipedia.org/wiki/Gapminder_Foundation
[spyder]: https://docs.spyder-ide.org/
[spyder-instal]: https://docs.spyder-ide.org/current/installation.html
[spyder-standalone]: https://docs.spyder-ide.org/current/installation.html#install-standalone
[anaconda-install]: https://www.anaconda.com/docs/getting-started/installation
[anaconda-tos]: https://anaconda.com/legal


