#Untangling Users

##Becoming Root with su

Here i learnt about the su(switch
user) command which grants me the root
access provided i know the password.
For this challenge, i was provided the
password to gain root access
Commands:
su
<hack-the-planet>
cat /flag

##Other users with su

By default, su provides access to root
shell. But if a username is provided
with the su command as an argument,
it switches authority to that user.
Commands:
su zardus
dont-hack-me
/challenge/run

##Cracking passwords

For this challenge, i have to switch
to user zardus using su command and
run the /challenge/run command, except
this time, I don't know the password.
I have to first crack his password.
Commands:
john /challenge/shadow-leak
su zardus
aardvark
/challenge/run

##Using sudo

In this challenge i learnt why sudo
is more powerful than su and why
the world now uses sudo instead of su.
sudo doesn't rely on passwords unlike su
thus reducing the risk of root password
getting leaked.
Commands:
sudo cat /flag
