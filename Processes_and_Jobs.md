# Processes and Jobs

  ## Listing Processes
  
    The /challenge/run file has been renamed. I am not allowed to
    ls into the directory. Hence to find the actual flag program,
    I have to list all the processes to find the actual program.
    Commands:
      ps -aux
      /challenge/2239-run-25033
  
  ## Killing Processes
  
    For this challenge I had to kill sleep process to stop
    /challenge/dont_run from running, and then run /challenge/run
    to get the flag
    Commands:
      ps -e
      kill 74
      /challenge/run
      
  ## Interrupting Processes
  
    I had to interrupt the processing of /challenge/run to get
    the flag
    Commands:
      /challenge/run
      <CTRL+C>
  
  ## Suspending Processes
  
    To run the program /challenge/run I had to create another 
    copy of itself. To do so, i had to supend the first operation
    and run the program again.
    Commands:
      /challenge/run
      <CTRL+Z>
      /challenge/run
      
  ## Resuming Processes
  
    To get the flag, I had to first run /challenge/run, then suspend
    it with <CTRL+Z> and then resume it through the fg command
    Commands:
      /challenge/run
      <CTRL+Z>
      fg
    
  ## Backgrounding Processes
  
    This was a good question i got an
    idea of Use the terminal to launch
    it, then suspend it, then
    background it with bg and launch
    another copy while the first is
    running in the background
    
  
  ## Foregrounding Processes
  
    Similiar to the previous one, but 
    this time I had to Foreground the
    process using fg after backgrounding
    it.
  
  
  ## Starting Backgrounding Processes
  
    Here, I learnt that it's not compulsory
    to suspend a process before running
    it in the background. It can be done
    by appending & to your command.
    Commands:
      /challenge/run &
  
  ## Process Exit Codes
  
    You can check the exit status of
    a code using "echo $?". If value 0
    is returned, it means the
    previous command was successfully
    executed. For this challenge, I had
    to get the exit code and use that
    as an argument to get the flag.
    Commands:
      /challenge/get-code
      echo $?
      /challenge/submit-code <EXIT-CODE>
    
  
