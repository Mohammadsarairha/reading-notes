# Bash Command Line Tutorials

## The Command Line

- A command line interface CLI processes commands to a computer program and you can communicate with all part with computer in the form of lines of text  it works pretty much like the GUI's on other systems ,  Actually CLI is more complicated than GUI but whit some practice you will leave GUI becuse ClI have many features like you can do multiple work and open many windows as you need in same time .

- In command line or terminal you write commands as keywork in CLI and command line return action as text in terminal.

- If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. echo is a command which is used to display messages.

```bash
user@bash echo $SHELL
/bin/bash
```

## Basic Navigation!

- We'll learn the basics of moving around the system. Many tasks rely on being able to get to, or reference the correct location in the system.
1. pwd : return directory path .

```bash
user@bash pwd
/home/ryan
```

2. ls : its shourcut of list that mean return all files in this directory.

```bash
user@bash ls
bin Documents public_html
```
More on Paths
- ~ (tilde) : This is a shortcut for your home directory.
- . (dot) : This is a shortcut for your current directory.
- .. (dotdot) : This is a reference to the parent directory.

```bash
user@bash ls ~/Documents

user@bash ls ./Documents

user@bash ls ls ../../
```

3. cd : Command to move around in the system .  

```bash
user@bash cd ~/Documents

user@bash cd ./Documents

user@bash cd ..
```

## Summary 

- pwd : Print Working Directory - ie. Where are we currently.
- ls : List the contents of a directory.
- cd : Change Directories - ie. move to another directory.


## More About Files

### Everything is a File : In linux it is considered everything is a file even keyborde key and screen and directorys , The following are common extensions :

- file.exe - an executable file, or program.
- file.txt - a plain text file.
- file.png, file.gif, file.jpg - an image.

### Linux is Case Sensitive : Such as GUI Can't have two and more file or directory with same name Ex :

```bash
user@bash ls Documents
FILE1.txt File1.txt file1.TXT

user@bash file Documents/file1.txt
Documents/file1.txt: ERROR: cannot open 'file1.txt' (No such file or directory)
```

## Spaces in names : Spaces in file and directory names are perfectly valid but we need to be a little careful with them .

- Example if you want to name directory Holiday Photos and in command try to move to this directory Linux dont know about it :

```bash
user@bash ls Documents
FILE1.txt File1.txt file1.TXT Holiday Photos

user@bash cd Holiday Photos
bash: cd: Holiday: No such file or directory
``` 

- If you need to solve this issue you need to use Quotes ' ' Ex:

```bash
user@bash cd 'Holiday Photos'
```

- backslash ( \ ) , This is another method you can use it if want to call directory have space Ex :

```bash
user@bash cd Holiday\ Photos
```

## Hidden Files and Directories
- How to create hide files just use . before file name Ex:

```bash
user@bash touch .test.txt
```

- Show Hidden Files From the Command Line Ex:

```bash
user@bash ls –a
```

## Summary 

- Everything is a file under,Linux Even directories.

- Linux is an extensionless system,Files can have any extension they like or none at all.

- Linux is case sensitive,Beware of silly typos.


# Manual Pages

## Introduction

- Fortunately for us there is an easy to use resource that can inform us about all the great things we can do on the command line, So you dont need to remember all command .

## The manual pages

- The manual pages are a set of pages that explain every command available on your system.

- You invoke the manual pages with the following command: man command name

```bash
user@bash man ls

Name
    ls - list directory contents
 
Synopsis
    ls [option] ... [file] ...
 
Description
    List information about the FILEs (the current directory by default). Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.
 
    Mandatory arguments to long options are mandatory for short options too.
 
    -a, --all
        do not ignore entries starting with .
 
    -A, --almost-all
        do not list implied . and ..
```

## Searching 
- It is possible to do a keyword search on the Manual pages , man -k <search term> , if you want to search in spasifac key Ex :

```bash
user@bash man -k printf

asprintf (3)         - print to allocated string
dprintf (3)          - formatted output conversion
fprintf (3)          - formatted output conversion
fwprintf (3)         - formatted wide-character output conversion
printf (1)           - format and print data
printf (3)           - formatted output conversion
snprintf (3)         - formatted output conversion
sprintf (3)          - formatted output conversion
swprintf (3)         - formatted wide-character output conversion
vasprintf (3)        - print to allocated string
vdprintf (3)         - formatted output conversion
vfprintf (3)         - formatted output conversion
vfwprintf (3)        - formatted wide-character output conversion
vprintf (3)          - formatted output conversion
vsnprintf (3)        - formatted output conversion
vsprintf (3)         - formatted output conversion
vswprintf (3)        - formatted wide-character output conversion
vwprintf (3)         - formatted wide-character output conversion
wprintf (3)          - formatted wide-character output conversion
```

## Summary 

- man <command> ,  Look up the manual page for a particular command.
- man -k <search term> , Do a keyword search for all manual pages containing the given search term.
- /<term> , Within a manual page, perform a search for 'term'

# File Manipulation

- The mkdir command in Linux/Unix allows users to create or make new directories.

```bash
mkdir [option] dir_name
```

-  Make a New Directory

```bash
user@bash mkdir Linux
```

- Create Multiple Directories

```bash
user@bash mkdir {test1,test2,test3}
```

- Make Parent Directories

```bash
user@bash mkdir –p Linux/parent1/parent2
```

- Creates a directory in the current location

```bash
user@bash mkdir –v Linux
```

## Files

- Create blank file 

```bash
user@bash touch Linux
```

- Copying a File : cp fileName destination

```bash
user@bash cp Linux ./parent1
```

Copying Directory : cp -r fileName destination

```bash
user@bash cp -r parent1
```

- Moving a File or Directory : you can move File and Directory without using -r .

```bash
user@bash mv Linux ./parent1
```

- Renaming Files and Directories : You can use mv command and rename file or directory in path Ex :

```bash
user@bash mv Linux ./parent1/Linux1
```

- Removing a File (and non empty Directories) : Use rm command its work just for file or empty directories

```bash
user@bash rm Linux 
```

Also for empty directory

```bash
user@bash rmdir Linux 
```

for directory not empty

```bash
user@bash rm -r Linux 
```

or

```bash
user@bash rm -rf Linux
```


## Summary 

- mkdir : Make Directory - ie. Create a directory.
- rmdir : Remove Directory - ie. Delete a directory.
- touch : Create a blank file.
- cp : Copy - ie. Copy a file or directory.
- mv : Move - ie. Move a file or directory (can also be used to rename).
- rm : Remove - ie. Delete a file.