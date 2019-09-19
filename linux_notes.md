# learning-linux-winfrednyoroka
learning-linux-winfrednyoroka created by GitHub Classroom

Basic Command lines to navigate the terminal


## Print working directory (pwd)

**pwd** _it means print working directory, you get the path of where you are in the directory


## List (ls)
**ls** _it means you are listing the items either they could be directories or subdirectopries or they could be files in your directory either the current directory or another directory away from where you are.

list can take up options
> ls -l
> ls-a
> ls -alh
> ls -R
## Changing the directory (cd)

**cd** _it involves changing your directory 

type the following:
cd  _it takes you to your home directory
cd ~ _it takes you to home directory
cd / _it takes you to root directory

cd . _it refers to your current directory

cd .. _it takes you to one directory back, actually the parent directory of where you are except when in the root directory


cd ../.. _it takes you two levels up from where you are currently

## Making a directory (mkdir)
**mkdir** _ this command enables one to create a directory
for instance: mkdir learning_unix
# NB: when naming directories in terminal avoid use of spaces, since terminal uses spaces when giving commands. instead make use of underscores
mkdir unixstuff
mkdir -p outer_git/inner_git
The above command line helps you create two directories at the same time where the second directory is hosted within the first directory and where any of the directories does not exist. it thus creates directories as needed.
# look for help
mkdir --help

# Looking for manuals for the command lines

__man__ helps the operator access the manual pages for each unix command 
e.g

man   | command
------- | ------
man | mkdir
man  | ls
man | grep
man | cp
man | cd

# Removing directories and files

Remove **rm** is a very dangerous command you have to use it carefully once deleted you will never recover yourfiles or directories

__NB__ you can only remove a directory when you are outside the directory
e.g **rmdir** inner_git

rmdir index* , remove all files starting with index

rm -i index* -when you use the option **-i** it asks you whether you really sure you want to delete the file or directory

# use of tab
click _tab_ once its used for autocompletion of file and directory names


# Create empty files
**touch** this command can be used in creating empty files

e.g touch learn_git.txt


# Moving files
**mv** -this command helps in moving files between directories. however, it does not make a copy of the file. 

In moving files then you must specify the file and the directory you want to move to

e.g mv notes.txt unixstuff/
 
 mv *.txt unixstuff/
 
 # NB: *  THIS IS A WILD CART, IT MEANS EVERYTHING FOR INSTANCE EVERYTHING WITH .TXT
 
 # Moving directories
 mv test1 test2
 
 in the above case test 1 and test 2 are directories. we are moving test 1 to test 2

## Copying files (cp)

cp _ it involves copying files into directories. the advantage is that you always retain a copy of your original file

cp 'input the file name' "preferred directory"
## NB: Input file may include the path showing where your directory is located
for instance : cp '~/Documents/NGS/COURSE_DATA/UNIX COURSE/MALARIA.FASTA' "."

# Renaming a file
 **mv**- can be used in renaming files for instance:
 
 mv inner.txt unixstuff/outer.txt (inner.txt is my old file name while oute.txt is my new file name; unixstuff is thelocation i am moving to and have it in a different name)
  
  # Viewing files
  1\. using the command **less**
  use the command **less** to view the contant of a file per page. this command allows you to view the file but you can never edit the file content
  **Echo** this command prints the statement on the screen
  
  e.g **echo** winfred is my name; it prints this statement on the terminal.
  however, ECHO can be used to redirect the statement into a file and we can use less command to view the file
  
  e.g **echo** "winfred is my name" > unixstuff.txt
  
  **less** unixstuff.txt
  
  **echo** "introduction to programming" >> unixstuff.txt
  when we make use of  **>>** we append the statement to the previous unlike when we use **>** which leads to overwriting the file.
  2\. using **cat**
  when we use **cat** command it displays all contents of the file of which the operator has no control of until it brings you another prompt.
   it can be used to combine multiple files and as well can be used to make a copy of the file
   
   # Combining files
   
   cat mal.fasta typ.fasta >combined.fasta
   cat *.fastq> combined.fastq
   
   # Making copies
   
   cat mal.fasta >mal2.fasta
   
  # Counting lines, words and characters in files
  
  we can use **ls -l** which gives us the number of lines and the size of the file in bytes
  
  instead we can use **wc** which gives us the lines, words and characters
  **wc** can take options for instance **wc -l** which give us the number of lines in the file
   
   **wc** readme.md
   **wc -l** readme.md
  
 # Editing small text files
 
 we make use of the **nano**
 
 **nano** unixstuff.txt
 
 down the terminal it provides the operator with options which we type in using Ctrl + X to mean exit
 
 $PATH envirnment variable
 **echo** can to be used in displaying environment variables
 e.g
 
 **echo** $USER 
 
 **echo** $PATH
 
 it displays the variables in the environmnt that  are directories containing the programs we run like the ls command in the bin
 
