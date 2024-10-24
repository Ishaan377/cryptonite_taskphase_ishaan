# Perceiving Permissions

  ## Changing File ownership
  
    This challenge taught me how people
    prevent others from touching files
    and how as hackers we can change 
    users and access their files.
    Commands:
      ls -l /flag
      chown hacker /flag
      cat /flag
  
  ## Groups and Files
  
    Learnt about Groups. Some files can
    be accessed by being part of the
    group that has authority over it.
    Similiar to the previous question,
    I used chgrp to change group to access
    the /flag file.
    Commands:
      ls -l /flag
      chgrp hacker /flag
      cat /flag
  
  ## Fun with Group names
  
    For this challenge, my group name has
    been randomised. I had to use id
    command to find my group and then
    change group to access the flag.
    Commands:
      id
      chgrp grp19509 /flag
      cat /flag
  
  ## Changing Permission
  
    In this challenge, I learnt how to
    change permissions for a file.
    Commands:
      ls -l /flag
      chmod o+r /flag
      cat /flag
  
  ## Executable Files
  
    Similiar to the previous one, but this
    time I have to modify the permissions
    of /challenge/run to make it executable
    by hacker.
    Commands:
      ls -l /challenge/run
      chmod u+x /challenge/run
      /challenge/run
  
  ## Permission Tweaking Practice
  
    For this challenge, i had to follow a
    set of instructions, to eventually
    access the flag
    Commands:
    hacker@permissions~permission-tweaking-practice:~$ chmod a+rwx /challenge/run
    /usr/bin/chmod: changing permissions of '/challenge/run': Operation not permitted
    NEEDED, BUT UNMET permissions of "/challenge/pwn": rw-rw-rw-
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    
    CURRENT, INCORRECT permissions of "/challenge/pwn": rw-r--r--
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    - the world doesn't have execute permissions
    
    You set the permissions incorrectly! Restarting the game!
    hacker@permissions~permission-tweaking-practice:~$ chmod go+w /challenge/run
    /usr/bin/chmod: changing permissions of '/challenge/run': Operation not permitted
    NEEDED, BUT UNMET permissions of "/challenge/pwn": rw-rw-rw-
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    
    CURRENT, INCORRECT permissions of "/challenge/pwn": rw-r--r--
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    - the world doesn't have execute permissions
    
    You set the permissions incorrectly! Restarting the game!
    hacker@permissions~permission-tweaking-practice:~$ chmod go+w /challenge/pwn
    You set the correct permissions!
    Round 1 (of 8)!
    
    Current permissions of "/challenge/pwn": rw-rw-rw-
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rw-rwxrw-
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod g+x /challenge/pwn
    You set the correct permissions!
    Round 2 (of 8)!
    
    Current permissions of "/challenge/pwn": rw-rwxrw-
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": r--r-xrw-
    * the user does have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod ug-w /challenge/pwn
    You set the correct permissions!
    Round 3 (of 8)!
    
    Current permissions of "/challenge/pwn": r--r-xrw-
    * the user does have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": r--r--r--
    * the user does have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod a-xw /challenge/pwn
    You set the correct permissions!
    Round 4 (of 8)!
    
    Current permissions of "/challenge/pwn": r--r--r--
    * the user does have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": r-xr-xr-x
    * the user does have read permissions
    - the user doesn't have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod a+x /challenge/pwn
    You set the correct permissions!
    Round 5 (of 8)!
    
    Current permissions of "/challenge/pwn": r-xr-xr-x
    * the user does have read permissions
    - the user doesn't have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": rwxr-xrwx
    * the user does have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    * the world does have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod uo+w /challenge/pwn
    You set the correct permissions!
    Round 6 (of 8)!
    
    Current permissions of "/challenge/pwn": rwxr-xrwx
    * the user does have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": rwxr-xr-x
    * the user does have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod o-w /challenge/pwn
    You set the correct permissions!
    Round 7 (of 8)!
    
    Current permissions of "/challenge/pwn": rwxr-xr-x
    * the user does have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": rwxrwxrwx
    * the user does have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    * the world does have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod og+w /challenge/pwn
    You set the correct permissions!
    You've solved all 8 rounds! I have changed the ownership
    of the /flag file so that you can 'chmod' it. You won't be able to read
    it until you make it readable with chmod!
    
    Current permissions of "/flag": ---------
    - the user doesn't have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    - the group doesn't have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    - the world doesn't have read permissions
    - the world doesn't have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permission-tweaking-practice:~$ chmod a+r /challenge/pwn
    hacker@permissions~permission-tweaking-practice:~$ /challenge/pwn
    hacker@permissions~permission-tweaking-practice:~$ cat /challenge/pwn
    hacker@permissions~permission-tweaking-practice:~$ chmod a+x /challenge/pwn
    hacker@permissions~permission-tweaking-practice:~$ /challenge/pwn
    hacker@permissions~permission-tweaking-practice:~$ chmod a+r /flag
    hacker@permissions~permission-tweaking-practice:~$ /flag
    ssh-entrypoint: /flag: Permission denied
    hacker@permissions~permission-tweaking-practice:~$ chmod u+r /flag
    hacker@permissions~permission-tweaking-practice:~$ /flag
    ssh-entrypoint: /flag: Permission denied
    hacker@permissions~permission-tweaking-practice:~$ ls -l /flag
    -r--r--r-- 1 hacker hacker 58 Oct  8 15:38 /flag
    hacker@permissions~permission-tweaking-practice:~$ chmod og-r /flag
    hacker@permissions~permission-tweaking-practice:~$ ls -l /flag
    -r-------- 1 hacker hacker 58 Oct  8 15:38 /flag
    hacker@permissions~permission-tweaking-practice:~$ cat /flag
    pwn.college{UR7lbqZLYL3985ne9sFjyQzqiMx.dBTM2QDL0kTN0czW}
  
  ## Permission Setting Practice
  
    Similiar to the previous one, but
    this time I have to set permissions
    instead of adding or removing.
    Commands:
    hacker@permissions~permissions-setting-practice:~$ chmod a+rwx /challenge/run
    /usr/bin/chmod: changing permissions of '/challenge/run': Operation not permitted
    NEEDED, BUT UNMET permissions of "/challenge/pwn": --xr--rwx
    - the user doesn't have read permissions
    - the user doesn't have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    * the world does have execute permissions
    
    CURRENT, INCORRECT permissions of "/challenge/pwn": rw-r--r--
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    - the world doesn't have execute permissions
    
    You set the permissions incorrectly! Restarting the game!
    hacker@permissions~permissions-setting-practice:~$ chmod u=x,o=rwx /challenge/pwn
    You set the correct permissions!
    Round 1 (of 8)!
    
    Current permissions of "/challenge/pwn": --xr--rwx
    - the user doesn't have read permissions
    - the user doesn't have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": r---wx--x
    * the user does have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    - the group doesn't have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    - the world doesn't have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u=r,g=wx,o=x /challenge/pwn
    You set the correct permissions!
    Round 2 (of 8)!
    
    Current permissions of "/challenge/pwn": r---wx--x
    * the user does have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    - the group doesn't have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    - the world doesn't have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": -w--wx--x
    - the user doesn't have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    - the group doesn't have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    - the world doesn't have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u=w /challenge/pwn
    You set the correct permissions!
    Round 3 (of 8)!
    
    Current permissions of "/challenge/pwn": -w--wx--x
    - the user doesn't have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    - the group doesn't have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    - the world doesn't have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": -wxrwxrw-
    - the user doesn't have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u=wx,g=rwx,o=rw /challenge/pwn
    You set the correct permissions!
    Round 4 (of 8)!
    
    Current permissions of "/challenge/pwn": -wxrwxrw-
    - the user doesn't have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": r-xrw--w-
    * the user does have read permissions
    - the user doesn't have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    - the group doesn't have execute permissions
    - the world doesn't have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u=rx,g=rw,o=w /challenge/pwn
    You set the correct permissions!
    Round 5 (of 8)!
    
    Current permissions of "/challenge/pwn": r-xrw--w-
    * the user does have read permissions
    - the user doesn't have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    - the group doesn't have execute permissions
    - the world doesn't have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": -wxrw--wx
    - the user doesn't have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    - the group doesn't have execute permissions
    - the world doesn't have read permissions
    * the world does have write permissions
    * the world does have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u=wx,o=wx /challenge/pwn
    You set the correct permissions!
    Round 6 (of 8)!
    
    Current permissions of "/challenge/pwn": -wxrw--wx
    - the user doesn't have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    * the group does have write permissions
    - the group doesn't have execute permissions
    - the world doesn't have read permissions
    * the world does have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": rw-r-xr-x
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u=rw,g=rx,o=rx /challenge/pwn
    You set the correct permissions!
    Round 7 (of 8)!
    
    Current permissions of "/challenge/pwn": rw-r-xr-x
    * the user does have read permissions
    * the user does have write permissions
    - the user doesn't have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    * the group does have execute permissions
    * the world does have read permissions
    - the world doesn't have write permissions
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": -wxr--rw-
    - the user doesn't have read permissions
    * the user does have write permissions
    * the user does have execute permissions
    * the group does have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    * the world does have read permissions
    * the world does have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u=xw,g=r,o=rw /challenge/pwn
    You set the correct permissions!
    You've solved all 8 rounds! I have changed the ownership
    of the /flag file so that you can 'chmod' it. You won't be able to read
    it until you make it readable with chmod!
    
    Current permissions of "/flag": ---------
    - the user doesn't have read permissions
    - the user doesn't have write permissions
    - the user doesn't have execute permissions
    - the group doesn't have read permissions
    - the group doesn't have write permissions
    - the group doesn't have execute permissions
    - the world doesn't have read permissions
    - the world doesn't have write permissions
    - the world doesn't have execute permissions
    hacker@permissions~permissions-setting-practice:~$ chmod u+r /flag
    hacker@permissions~permissions-setting-practice:~$ cat /flag
    pwn.college{giL09gGoCTabWE70g7816jEM8Nk.dNTM5QDL0kTN0czW}
  
  ## The Suid Bit
  
    Learnt about the SUID permissions
    bit that allows the user to run
    program as the owner of that
    program's file. For this challenge
    I had to provide the SUID
    permission to the /challenge/getroot
    program and access the flag
    Commands:
      chmod u+s /challenge/getroot
      ls -l /challenge/getroot
      /challenge/getroot
