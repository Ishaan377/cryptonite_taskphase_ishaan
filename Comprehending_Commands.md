# Comprehending Commands
 
  ## cat: not the pet, but the command
  
    I understood that the cat command reads the terminal input.
    I used cat flag to get the flag
  
  ## catting absolute paths
  
    I used the absolue path of flag and found the flag by running 
    this command: cat /flag
  
  ## more catting practice
  
    Found the flag using the absolute path and without cding into the file directory
  
  ## grepping for a needle in a haystack
  
    Here I learnt about the grep command that helps 
    in searching for a certain string, given as an argument, 
    in a file. After grepping for the string pwn.college I found the flag.
  
  ## listing files
  
    In this lesson, I came across the listing files(ls) command. This command, when run,
    provides the list of files in the current directory. After using ls command in the 
    /challenge directory, I found the file containing flag
  
  ## touching files
  
    I was told to create two files(/tmp/pwn and /tmp/college) to be able to run the
    /challenge/run file to get the flag. This was done by using the touch 
    command which is used to create files.
    syntax: touch <file_name>\
  
  ## removing files
  
    Just like touch, a command to create files, there exists a 
    command to remove files, namely, rm
    Syntax: rm <file_name>
    Only after removing the file delete_me was I able to run 
    the file /challenge/check to get the flag
  
  ## hidden files
  
    I used the cd command to go the / directory
    then I used the "ls -a" command to search for hidden files
    and then I read the hidden flag file using cat command
  
  ## An Epic File System Quest
  
    Start by navigating to the root directory using cd /. Then, use ls to list the files
    in that directory. 
    To view the content of any file, use cat, and cd to enter any specified directories. 
    Repeat these steps as needed.
    For files with a time delay, run ls to display them. 
    For hidden files, use "ls -a". If a file is "trapped" or inaccessible, list its directory with `ls <directory>`. 
    Use "cat <directory>/<filename>" to uncover the next clue. 
    Continue this process to eventually obtain the flag.
  
  ## making directories
  
    Used mkdir command to make a directory.
    Used touch command to create file
  
  ## finding files
  
    I used "find / -name flag" to search the entire filesystem for a file named "flag". 
    After locating it, I executed all the available files to eventually retrieve the flag.
  
  ## linking files
  
    I created a symbolic link using "ln -s /flag /home/hacker/not-the-flag" 
    and then ran "/challenge/catflag" to trick it into revealing the flag.
