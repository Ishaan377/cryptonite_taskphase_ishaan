#Pondering Paths

##The Root

Invoked the pwn directory using its absolute path- \pwn

##Program and absolute paths

This time i invoked 'run' file in the challenge directory using its absolute path- \challenge\run

##Position thy self

After trying out /challenge/run , I was told that im in the wrong directory.

After switching to the right directory using the cd(change directory) command, I ran the /challenge/run command to finally get the flag.

##Position elsewhere

Similiar to the previous one, after trying to run the /challenge/run in the wrong directory, i was notified to change my directory to /sys.

After doing so using cd comnmand, i ran the /challenge/run to get the flag

##Position yet elsewhere

Similiar to the previous one, after trying to run the /challenge/run in the wrong directory, i was notified to change my directory to /tmp.

After doing so using cd comnmand, i ran the /challenge/run to get the flag

##implicit relative paths, from /

Similiar to the previous one, after trying to run the /challenge/run in the wrong directory, i was notified to change my directory to /.

After doing so using cd comnmand, i ran the challenge/run to get the flag(since the path is relative to / directory, the command is 

challenge/run instead of /challenge/run)

##explicit reative paths, from /

Here I understood that the relative paths can also begin with ./ otherwise its very similiar to the previous one

##implicit relative path

I learnt about a safety measure of linux that prevents core system utilities from running accidentally.

First used cd command to get into the /challenge directoruy and then executed the run file using ./run

##home sweet home

After setting my cwd as my home directory and the proceeded to use the /challenge/run command with a file as

an argument with its absolute path. This provided me the flag.
