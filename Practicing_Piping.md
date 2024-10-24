# Practicing Piping

  ## Redirecting Output
  
    As the name suggests, This challenge is about
    redirecting output into a file. While "echo hi"
    gives the output "hi", if its paired with > character
    you can redirect that output to a file, whose name
    is provided as an argument. To obtain the flag,
    I had to redirect PWN from "echo PWN" to the
    file COLLEGE.
  
  ## Redirecting more output
  
    Similiar to the previous one, but this time, i
    had to redirect the output of /challenge/run to
    myflag to obtain the flag. Also taught the difference
    between output given over stdout and stderr.
  
  ## Appending output
  
    When we use > character to redirect output to
    a file, it truncates the file and overwrites it
    with the latest data. To avoid this, the append mode is
    used(>>). For this challenge i had to append the second 
    half of the flag to /home/hacker/the-flag while running
    the /challenge/run program.
  
  ## Redirecting 
  
    This challenge explains the > character in detail.
    I learnt about the file descriptor numbers and
    how they form a part of the piping function.
    For this challenge i had to redirect the standard errors
    from /challenge/run to instructions and the standard
    output to myflag, to get the flag.
    Commands:
      /challenge/run > myflag 2>instructions
      cat myflag
  
  ## Redirecting input
  
    Learnt about the < character, which redirects input
    from files. For this challengge i had to redirect
    COLLEGE into the file PWN using the echo function
    and then redirect input from PWN to the
    /challenge/run program
  
  ## Grepping stored results
  
    I redirected the output of the command "/challenge/run" 
    to ">/tmp/data.txt" using >. After that, I ran 
    "grep pwn.college /tmp/data.txt" to extract the flag.
  
  ## Grepping live outputs
  
    Learnt about the pipe character(|)
    Eliminates the requirement of a file to store output,
    unlike the previous challenge.
    Takes stdin from program on the left of it and
    provides stdout for the program on the right of it
    Commands:
      /challenge/run | grep pwn.college
  
  ## Grepping errors
  
    Similiar to the previous one, but this time,
    I had to grep from the stderr of /challenge/run
    to obtain the flag.
    Command:
      /challenge/run 2>& 1 | grep pwn.college
  
  ## Duplicating piped data with tee
  
    I used "/challenge/pwn | tee t | /challenge/college" 
    to pipe "/challenge/pwn" to "/challenge/college"
    but intercepted it by using tee t , then i used cat t to get the secret value
    Then i used "/challenge/pwn --secret [kCCjr_M0] | tee tmp | /challenge/college" to get the flag
  
  ## Writing to multiple programs
  
    I used the "/challenge/hack" command and duplicated its 
    output as an input to "/challenge/the" and "/challenge/planet"
    Commands:
      /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
  
  ## split-piping stderr and stdout
  
    In this challenge, I needed to redirect stdout to /challenge/planet and stderr to /challenge/the, while keeping them separate.
    I had to was combine  >(), 2>, and piping. The | operator normally links stdout to another program’s stdin, but the goal was to avoid mixing stdout and stderr.
    Commands:
      /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
