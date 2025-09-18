# Level 4 --> 5

## Task
The password for the next level is stored in the only human-readable file in the `inhere` directory. 

## Solution
1. `ls`
   - List contents of current directory
2. `cd inhere`
   - Changes directory to `inhere`
3. `ls -a`
   - Lists contents of current directory including hidden files
4. `file ./*`
   - Lists the file types of all the files in the current directory
   - `file` asks for the file type
   - `.` needed as files start with `-`
   - `/` is a path separator and is required to prevent the command only printing files starting with `.`
   - `*` is referred to as a wildcard and gets all the filetypes in the current directory
5. The file containing human readable text (-file07) will have "ASCII text" as the filetype
6. `cat ./-file07`
   - Prints contents of file
7. Password - 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
