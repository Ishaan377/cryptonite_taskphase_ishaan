#Chaining Commands

##Chaining with Semicolons

Here i learnt how to chain multiple
commands using the semicolon. For
this challenge, i had to chain
/challenge/pwn and /challenge/college
to get the flag.

##Your First Shell Script

To avoid confusion from chaining
multiple commands together, we can
write all this command to a shell,
and then run the shell with the bash
command.
Commands:
touch x.sh
echo "/challenge/pwn" >> x.sh
echo "/challenge/college" >> x.sh
bash x.sh

##Redirecting Script Output

Similiar to the previous one, except
for this challenge, I had to pipe
the output to the /challenge/solve
command.
Commands:
touch x.sh
echo "/challenge/pwn" >> x.sh
echo "/challenge/college" >> x.sh
bash x.sh | /challenge/solve

##Executable Shell Scripts

Here, I learnt that I can ignore
the bash command if my script is
executable. For this challenge,
I had to make an executable script
that invokes the /challenge/solve
command.
Commands:
touch solve.sh
echo "/challenge/solve" >> solve.sh
chmod +x solve.sh
./solve.sh
