# File Globbing

  ## Matching with *
  
  I learnt about the glob character *
  When a directory/file name is executes with * , it gets replaced
  with the matching name. In this challenge, I had to
  cd into /challenge withput specifiing more than 4 characters
  Commands:
    cd /ch*
    /challenge/run
  
  ## Matching with ?
  
  Similiar to the previous one but isntead of replacing
  multiple matching characters in case of *, ? just gets
  replaced by one character.
  Commands:
    cd /?ha??enge
    /challenge/run

  ## Matching with []
  
  Similiar to the previous one, except, unlike ?,
  [] replaces the place with a single matching character, it chooses
  matching characters from a given set.
  Command:
    cd /challenge/files
    /challenge/run file_[bash]
    Here the file names were file_b, file_a, file_s, file_h.
  
  ## Matching paths with []
  
  Again, similiar to the previous one, but this time I had
  to expand the whole path to the file while globbing
  with [], from my home directory.
  Command:
    /challenge/run /challenge/files/file_[bash]
  
  ## Mixing globs
  
  In this challenge, i had to use multiple globs to obtain
  the flag.
  Commands:
    cd /challenge/files
    /challenge/run [pec]*

  ## Exclusionary globbing
  
  Here, I learnt about a new feature of [] glob which
  checks for files not containing certain characters.
  Syntax: [!<exclusionary_characers>]
  Commands:
    cd /challenge/files
    /challenge/run [!pwn]*
