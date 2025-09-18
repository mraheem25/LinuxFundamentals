# File Permissions

#### Managing file permissions is key for maintaining system security by preventing unauthorised access to restricted files. To view the file permissions of your current working directory, execute the command `ls -l` 

### Notation (String representation)
 "`-`    $\color{#FF0000}{rwx}$    $\color{#00FF00}{rwx}$    $\color{#0000FF}{rwx}$",  where:
  - `-` represents a directory (d) or file (`-`)
  - `r` = read (view file contents)
  - `w`= write (modify file contents)
  - `x` = execute (run file as a program)
  - $\color{#FF0000}{rwx}$ - represents user rights (file owner/person who created the file)
  - $\color{#00FF00}{rwx}$ - represents group rights (users belonging to a group with similar permissions)
  - $\color{#0000FF}{rwx}$ - represents other rights (all the other users on the system)

### Binary and Octal representation

Binary representation assigns a value of either 1 or 0 to a placeholder

Octal representation uses base 2 and assigns a value of 4 (r), 2(w), or 1(x) to a placeholder. User, group and other are each given a value based on the summation of the placeholder values

**Example**
- `rwx r-- -w-` - string representation
- `111 100 010` - binary representation
- `742` - octal representation

### Changing Permissions

To change permissions of a file or directory, the `chmod` command must be used. There are two methods of using the chmod` command, symbolic and numeric

Symbolic 
- `chmod +x (filename)` - executable permission for user, group and other
- `chmod u+x,g+r,o-w (filename)` - user gets executable permission, group gets readable permission and others have the write permission removed

Numeric (octal representation)
- `chmod 750 (filename)` - user gets full permission (4+2+1=7), group gets read and executable permission(4+1=5) and other has no permissions
