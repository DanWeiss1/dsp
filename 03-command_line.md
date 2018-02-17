# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > pwd shows the current directory
> > mkdir creates a directory
> > rm -r dirname would delete the directory 'dirname'
> > touch file1.txt would create a file in the current directory called "file1.txt"
> > rm file1.txt would delete the file.txt in the current directory
> > mv file1.txt file2.txt would rename file1.txt as file2.txt (mv also can move files between directories)
> > ls -a lists all the files in a directory including hidden files
> > cp /dir1/file1.txt /dir2 would copy file1.txt in dir1 into dir2
> > nano file1.txt would open file1 to be edited in the terminal
> > env lists the current environment 

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > ls lists all non hidden files and directories in the current directory
> > ls -a lists hidden and non hidden files and directories in the current directory
> > ls -l lists all files in the current directory along with metadata about the file size, last modification date, owner
> > ls -lh would do the same as above but print the output larger
> > ls -lah would combine the above options, listing all hidden and non hidden files and printing the metadata about each in larger size
> > ls -t lists the files in order of the most recent modification date
> > ls -Glp G is the option to color code the directories. l prints metadata.  p adds a backslash to directories.  so ls -GLP prints non-hidden files and directories with metadata and directories are printed in blue with a backslash

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -1 displays each item on its own row
> > ls -R displays all subdirectories
> > ls -r dipslays files in reverse order
> > ls -d displays only files with directories
> > ls -C displays files in a column format

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs breaks a list of input into sublists to avoid an error with a command that is too long and to allow you to apply a bash command to many files at once
> > one example might be if you wanted to remove all files containing the extension '.c' in the current directory and all subdirectories.  you could type  $ find . -name "*.c" | xargs rm -rf

 

