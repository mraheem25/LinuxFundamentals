# Level 6 --> 7

## Task 

The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Solution

1. `find -type f -size 33c -user bandit7 -group bandit6`
   - Using the same construct as in level 5 with the addition of specifying a user and group
2. `cat /var/lib/dpkg/info/bandit7.password`
   - Prints the contents of the file
3. Password - morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
