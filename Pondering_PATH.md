#Pondering PATH

##The PATH variable

In this challenge, the /challenge/run
command deletes the flag using rm.
To prevent this from happening, I
first had to disrupt the PATH variable
so it can't find the rm command.
Commands:
PATH=""
/challenge/run

##Setting PATH

In this challenge, the /challenge/run
requires the win command to provide
the flag. But the win command exists
in /challenge/more-commands/ ditectory.
To access the win command, I had to 
set the PATH to /challenge/more-commands/.
Commands:
PATH=/challenge/more_commands/
/challenge/run

##Adding Commands

This was one of the toughest one so
far... Had to search on yt to get the
details.
Commands:
ln -s /usr/bin/bash ./win
PATH=/home/hacker/:$PATH
/challenge/run
cat /flag

##Hijacking Commands

This was like the previous one, but
even complicated. Again, had to use
chatgpt to find this one out.
Commands:
rm rm
ln -s /usr/bin/bash ./rm
PATH=/home/hacker/:$PATH
/challenge/run
