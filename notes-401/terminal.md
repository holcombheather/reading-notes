# Practice in the Terminal 

- [Bash Command Line Tutorials](https://ryanstutorials.net/linuxtutorial/)
- [Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

***

1. **The Command Line**
    - Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called **bash** which stands for Bourne again shell. This tutorial will assume you are using bash as your shell.
    - If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. **echo** is a command which is used to display messages.

***

2. **Navigation**
    - `pwd`
    Print Working Directory - ie. Where are we currently.
    - `ls`
    List the contents of a directory.
    - `cd`
    Change Directories - ie. move to another directory.

    #### Important Concepts 
    - **Relative Path**
    A file or directory location relative to where we currently are in the file system.
    - **Absolute Path**
    A file or directory location in relation to the root of the file system. 

***

3. **More About Files**
    - `file`
    obtain information about what type of file a file or directory is.

    - `ls -a`
    List the contents of a directory, including hidden files.

    #### Important Concepts 
    - **Everything is a file under Linux**
    Even directories.
    - **Linux is an extensionless system**
    Files can have any extension they like or none at all.
    - **Linux is case sensitive**
    Beware of silly typos.

***

4. **Manual Pages**
    - `man <command>`
    Look up the manual page for a particular command.

    - `man -k <search term>`
    Do a keyword search for all manual pages containing the given search term.

    - `/<term>`
    Within a manual page, perform a search for 'term'

    - `n`
    After performing a search within a manual page, select the next found item.

        #### Important Concepts 
    - **The man pages are your friend**: Instead of trying to remember everything, instead remember you can easily look stuff up in the man pages.

***

5. **File Manipulation** 

    - `mkdir`
    Make Directory - i.e., Create a directory.

    - `rmdir`
    Remove Directory - i.e., Delete a directory.

    - `touch`
    Create a blank file.

    - `cp`
    Copy - i.e., Copy a file or directory.

    - `mv`
    Move - i.e., Move a file or directory (can also be used to rename).

    - `rm`
    Remove - i.e., Delete a file.

    #### Important Concepts 
    - **No undo**: The Linux command line does not have an undo feature. Perform destructive actions carefully.
    - **Command line options**: Most commands have many useful command line options. Make sure you skim the man page for new commands so you are familiar with what they can do and what is available.
