# Programs & Binaries

Commands such as ls, grep, cat and echo are small programs. These programs are written in programming language and compiled into a format that the computer can execute called a binary
### Program 
   - Written by developer to perform specific tasks
### Binary
   - Compiled versions of programs that the computer can run directly.
## Behind the scenes of running ls

Step 1: Shell interpretation
  - Shell understands we want to run the ls program
    
Step 2: Finding the program
  - Shell searches for ls program in certain directories, which are listed in the path environemnt variable
    
Step 3: Executing the program
  - Once ls program is found, it is executed by listing the contents of the current directory and displaying them on the terminal

## Path Environemnt Varibale

The path environment variable tells the shell in which directories in needs to look for these commands/programs
    
The command `echo $PATH` prints the following:
`/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin`
where bin represents a binary (folder)
