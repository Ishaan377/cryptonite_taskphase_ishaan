#Processes and Jobs

##Listing Processes

The /challenge/run file has been renamed. I am not allowed to
ls into the directory. Hence to find the actual flag program,
I have to list all the processes to find the actual program.
Commands:
ps -aux
/challenge/2239-run-25033

##Killing Processes

For this challenge I had to kill sleep process to stop
/challenge/dont_run from running, and then run /challenge/run
to get the flag
Commands:
ps -e
kill 74
/challenge/run

##Interrupting Processes

I had to interrupt the processing of /challenge/run to get
the flag
Commands:
/challenge/run
<CTRL+C>

##Suspending Processes

To run the program /challenge/run I had to create another 
copy of itself. To do so, i had to supend the first operation
and run the program again.
Commands:
/challenge/run
<CTRL+Z>
/challenge/run

##Resuming Processes

To get the flag, I had to first run /challenge/run, then suspend
it with <CTRL+Z> and then resume it through the fg command
Commands:
/challenge/run
<CTRL+Z>
fg


