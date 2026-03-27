# Meeting Two Agenda
Agenda for meeting two 3/27/2026

Topics that need to be covered:

- Mapping Ubuntu fs as network drive
- Installing an IDE
- Basic Linux filesystem navigation and commands
    - ls
    - cd
    - mkdir
        - create datascienceclub dir
    - apt
        - update
        - upgrade
        - install
- Install mini-forge
- Introduction to using Git and Github
    - version management. What is it? Why do we need it?
    - git clone
    - git init
    - git add / commit
    - git push
    - git merge
    - git rebase
    - git pull
- Python!
    - The Python interpreter. Interpreted vs. Compiled languages
    - Data Types
    - Variables
    - Conditionals
    - Functions

(I wanna get into some actual material so as not to make the first two meetings just boring slop. Maybe I will replace the Anaconda section with an intro to Python lesson. Come up with a small, fun mini-project that will hit on the beginner aspects of coding.)

Potential Projects?:
    Should hit on conditionals, loops, maybe lists and dicts, 


## Mapping Ubuntu fs as a Network Drive

In order to easily access your Ubuntu filesystem from Windows, it is recommended that you map your Ubuntu filesystem as a network drive.

- Open your file explorer, and navigate to `This PC`
- Click on the menu option titled `Computer`, and then select `Map Network Drive`
- Select whichever drive letter you would like
- type in `\\wsl$\Ubuntu-20.04` and then click `Finish`

This will be very useful later on when using VSCode / any other application you wish to modify your Ubuntu files from. For example, if you wish to open the file `example.txt` that lives in your Ubuntu home directory from VSCode, you can select the new network drive you just made, and then navigate to `/home/userName/example.txt`

## Installing an IDE

We will be installing VSCode as our IDE.

Follow this link to find the VSCode installer, and install it onto your Windows machine: https://code.visualstudio.com/download

WARNING: While installing, you will be asked if you would like to Select Additional Tasks during installation. When this happens, be sure to check the `Add to PATH` option. This will allow you to easily open VSCode from WSL. Not doing this will make your life so much harder, I promise.

NOTE: If you already have VSCode installed, but did not add it to your PATH on installation, you will need to add the location to the VSCode executable to your PATH manually. If you are unsure of how to do this, contact the SRO President or drop a message in the Discord and someone will be able to assist you.

After VSCode is finished installing, we will need to install the WSL extension in order to use VSCode from WSL. Launch the newly installed VSCode from Windows. Click on the extensions icon in the left navigation bar (it should look like 4 squares, with one disconnected from the rest). In the search bar, search "WSL." You should see an extension with a white penguin sitting in front of a blue background. Select it and wait for it to install. After that, close VSCode and restart your Ubuntu terminal.

After restarting your terminal, you should now be able to open VSCode from the Ubuntu terminal by simply running the `code .` command

## Linux Commands and File System Navigation

There are a few core commands that you will need to become familiar with in order to use Linux. Most of these commands have to deal with navigating and gathering information from your Linux filesystem.

Of the thousands of commands Linux comes installed with, the most basic and fundamental to know are the following:

- pwd : print the name of the current working directory
- ls : List the contents of a dirctory
- cd : Change directory
- mkdir : Make a new directory
- mv : move a file or directory to a new location
- cp : copy a file or directory to a new location
- apt : Default package manager for Debian based Linux distributions

Type in your current terminal the `ls` command. As

## Installing miniforge

See github org README.md
