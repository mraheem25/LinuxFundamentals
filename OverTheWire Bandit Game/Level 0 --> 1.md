# Level 0 --> 1

## Task
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH.

## Solution
1. `ssh bandit0@bandit.labs.overthewire.org -p 2220`
   - Logs into the user bandit0
2. `ls`
   - List contents of current directory
3. `cat readme`
   - Prints contents of readme file
4. Password - ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
