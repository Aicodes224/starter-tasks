Bandit

Link to the website: https://overthewire.org/wargames/bandit/bandit0.html


Bandit Level 0
Level Goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

ssh bandit0@bandit.labs.overthewire.org -p 2220

Enter ‘yes’

Username: Bandit0

Password: Bandit0



Bandit Level 0 → Level 1
Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

Run ‘ls -alps’

I run ‘cat readme’

I got the level 1 password

Level 1 password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Run ‘exit’ to logout



Bandit Level 1 → Level 2
Level Goal
The password for the next level is stored in a file called - located in the home directory

ssh bandit1@bandit.labs.overthewire.org -p 2220

Run the level 1 password:boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Run ‘cat ./-’

Level 2 password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9



Bandit Level 2 → Level 3
Level Goal
The password for the next level is stored in a file called spaces in this filename located in the home directory

ssh bandit2@bandit.labs.overthewire.org -p 2220

Run level 2 password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Run ‘ls -al’

Run ‘ cat \  spaces\  in\  this\  filename’

Level 3 password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK



Bandit Level 3 → Level 4
Level Goal
The password for the next level is stored in a hidden file in the inhere directory.

ssh bandit3@bandit.labs.overthewire.org -p 2220

Run level 3 password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Run ‘ls -alps’

Run ‘cd inhere/’

Run ‘ls -al’

Found the ‘.hidden’ file in inhere dictionary

Run ‘cat.hidden’

Level4 password: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

‘exit’


Bandit Level 4 → Level 5
Level Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

ssh bandit4@bandit.labs.overthewire.org -p 2220

Run level 4 password: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

Run ‘ls -alps’

Run ‘cd inhere/’

Run ‘ls’

Run ‘find .type f | xargs file

We see that file07 has ASCII Text

Run ‘cat ./-file07’

Level 5: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

‘Exit’



Bandit Level 5 → Level 6
Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
human-readable
1033 bytes in size
not executable

ssh bandit5@bandit.labs.overthewire.org -p 2220

Run level 5 password: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

Run ‘ls’

Run ‘cd inhere/’

Run ‘find .type f -size 1033c ! -executable’

We get ‘./maybehere07/.file2’

Level 6: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

‘exit’



Bandit Level 6 → Level 7
Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties: owned by user bandit7,owned by group bandit6, 33 bytes in size

ssh bandit6@bandit.labs.overthewire.org -p 2220

Run level 6 password: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

Run ‘find / -type f -user bandit7 -group bandit6 -size 33c’

We get the password

Level 7: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

‘exit'



Bandit Level 7 → Level 8
Level Goal
The password for the next level is stored in the file data.txt next to the word millionth.

ssh bandit7@bandit.labs.overthewire.org -p 2220

Run level 7 password: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

Run ‘ls -alps’

‘Strings data.txt | grep “millionth” ‘

We get the password

Password: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

‘exit’



Bandit Level 8 → Level 9
Level Goal: The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

ssh bandit8@bandit.labs.overthewire.org -p 2220

Run level 8 password: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

Run ‘cat data.txt’

 Run ‘sort data.txt | uniq -c’ to find the only line that occurs once.
 
(-c is ‘count’, the command will count the number of times the line is repeated)

Level 9 password:  UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

‘Exit’



Bandit Level 9 → Level 10
Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

ssh bandit9@bandit.labs.overthewire.org -p 2220

Run level 9 password:UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

Run ‘ strings data.txt | grep "=" ‘

We get the Level 10 password: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

‘exit’ and logout




   



 







