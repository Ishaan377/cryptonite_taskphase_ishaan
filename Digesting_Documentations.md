# Digesting Documentation

  ## Learning from Documentation
  
  This lesson taught me the basics of using arguments for commands.
  I ran the /challenge/challenge program using the argument --giveflag
  to get the flag
  
  ## Learning Complex Usage
  
  This modukle dealt with the usage of complex arguments-
  Arguments with an argument of its own
  I had to run the /challenge/challenge program with the argument
  --printfile which had another sub-argument specifying the file to be
  printed, namely /flag.
  
  ## Reading Manuals
  
  Here, I learnt about the manual for commands, which can be invoked
  with the command: man <command_name>
  To obtain the flag, I had to read the manual of program challenge
  to fimd thye correct syntax and arguments required to reach the flag.
  The command was /challenge/challenge --osvbnk 105
  
  ## Searching Manuals
  
  As the name suggests, this module focussed on searching a manual.
  using / or ? we are able to search for specific strings in a 
  manual. This time i had to search for an argument for
  /challenge/challenge using the keyword flag.
  command: 
  /challenge/challenge --jh

  ## Searching For Manuals
  
  Similiar to the previous one, except this time, the manual is unknown.
  Steps to solve:
  Perform "man man"
  Obtain the argument -k to search for keywords
  Execute "man -k challenge" to find the manual(npgtzmxdjc)
  Execute "man npgtzmxdjc" to find argument --npgtzm
  Execute /challenge/challenge --npgtzm 848 to get flag
  
  ## Helpful Programs
  
  Teaches the use of --help argument.
  Steps to solve:
  Execute "/challemnge/challenge --help"
  Find the required arguments
  Execute "/challenge/challenge -p" to get the secret value(396)
  Execute "/challenge/challenge -g 396" to get flag
  
  ## Help For Builtins
  
  Some commands are built into the shell. This module teaches the
  use of help in this context.
  Steps to Solve:
  Execute "help challenge" to get secret arument and value
  Execute "challenge --secret 4Js4Z2oz" to get flag
