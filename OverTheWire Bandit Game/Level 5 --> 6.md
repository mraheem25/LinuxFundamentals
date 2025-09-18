# Level 5 --> 6

## Task
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

## Solution
1. `ls`
   - List contents of current directory
2. `cd inhere`
   - Changes directory to `inhere`
3. `ls -a`
   - Lists contents of current directory including hidden files
4. `find . -type f -size 1033c ! -executable -exec file {} \; | grep ASCII`
   - There are multiple directories with multiple files. Therefore we must use `find` command.
   - `.` looks for files in current directory
   - `-type f` specifies we are looking for a file
   - `-size 1033c` specifies we are looking for a file with a size of 1033 bytes, where `c` = bytes
   - `! -executable` specifies that the file is not (`!`) executable (`-executable`)
   - `-exec file {} \;` means that for each file found, run this command with the file as an argument
     - `file` asks for the file type of each file found with the specifications outlined above
     - `{} \;` - pathname used in find constructs and ends the `-exec` option of the find sequence, where `{}` is a placeholder for output text
   - `| grep ASCII` from the output of the previous command, this command sequence will search for the filetype `ASCII`
     - `|` is referred to as a pipe and passes the output of the file command to the input of the `grep` commnad
     - `grep` searches for the file
5. `cat ./maybehere07/.file2`
   - Prints contents of the file
7. Password - HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

