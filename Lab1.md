# Lab Task

(All this information is on the ee160 webstie)

## Making teams
1. Make teams of 3. Team of 2 will be allowed if there is not enough people.

## Logging to Wiliki
1. Use Putty if window or use Terminal in MAC

If in MAC
```
ssh frendy@wiliki.eng.hawaii.edu
```

If in Window - Putty
```
In Host Name: wiliki.eng.hawaii.edu
Port: 22

Then Save:
Then fill your username and password.
```
##  "Setting Up Your Environment"
Now Create a directory, type the following:
```
mkdir EE160

PS: 

You can replace EE160 for the name of the new folder
mkdir means Make a Directory
```

## Unix Commands

### Tips
Write the following for more information of the command:

```
man name_of_Command
```

### Navigating in Unix
- pwd
    - print name of current/working directory

- cd
    - change directory (Move to a different folder)

- ls
    - list directory contents

- cat
    - concatenate files and print on the standard output
    - cat test test1 test2 > test3
        - This will create a file called test3 and all output will be redirected in a newly created file

### Managing files
- mkdir
    - make directory
- cp 
    - copy files and directory
- mv 
    - move (rename files)
- rm
    - rempve files

## Vim (Text editor)
Type the following in wiliki to find a manual for vi

```
vimtutor
```

TLDR
```
Press I, to start typing.

Press ESC and then type !q to quit

Press ESC and then type !wq to save and leave

```

## ELM
```
Type: elm
To send: m
After finishing typing: CTRL - X
Sends a real email

use q to quit

Or y
```

```
elm -s subject_name [Name_Of_Email, you can just type UH Username]
```