## Linux Commands
  - Are textual instruction that tells the OS what to do
  - Are enetered into the terminal/command line interface
  - Are case sensitive
  - Have various options and arguments which modify their behaviour. These can be found in the manual page.
    - Type `man (command)` into the terminal to get a breakdown of the command

## Basic commands
  - `ls` - Lists the contents of the current working directory
  - `pwd` - Prints the current working directory
  - `cd` - Change directory
  - `mkdir` - Create directories
  - `rmdir` - Remove empty directories;
  - `rm` - Remove files or remove directories and contents recursively (-r)
  - `cp` - copy files and directories (-r)
  - `mv` - move (rename) files
  - `touch` - Create empty files and update the timestamp of existing files.
  - `echo` - Display a line of text or a string that is passed as an argument and redirect (`>`) text to a file. Append operator (`>>`) is used to add additional text and prevent existing text to be overwritten
  - `cat` - concatenate files and print on the standard output. It reads data from files and outputs their contents. This command can also be used to combine multiple files into one and append the contents of one file into another
  - `head` - Prints first 10 lines. To print the first x lines, type `head -n x`
  - `tail` - Prints last 10 lines. To print the last x lines, type `tail -n x`

 ## Sudo Command
 `**Sudo**` - **S**uper **U**ser **Do** 
   - Allows you to execute commands as superuser/rootuser
   - Only permitted users can use sudo
#### When to use
   - Required to create new users and groups
   - Manage permissions
   - Updating and/or installing packages: `sudo apt install <package>`
   - Editing system configuration files: `/etc/hosts`, `/etc/passwd`
     - Useful when you need to `vim` into a file that is in the `/etc` folder

           
