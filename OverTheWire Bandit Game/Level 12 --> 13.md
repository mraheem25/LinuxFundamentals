# Level 12 --> 13.md

## Task
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv

# Solution
1. `mktemp -d`
   - Creates a temporary file with the filepath `/tmp/tmp.L9U9Z3nUwG`
   - `mktemp` creates a temporary file or directory (`-d`) under /tmp
3. `cp data.txt /tmp/tmp.L9U9Z3nUwG`
   - Copy the contents of data.txt into `/tmp/tmp.L9U9Z3nUwG`
4. `cd /tmp/tmp.L9U9Z3nUwG`
   - Change directories to enter into the specified location
5. `xxd -r data.txt > stage1`
   - `xxd` - makes a hexdump of a given file or can do the reverese (`-r`)
   - `>` is used to redirect contents of one file to another 
6. `file stage1`
   - Checking the filetype of stage1
   - stage1 is gzip compressed data
7. `gzip -dc stage1 > stage2`
   - `gzip` - used to compress or decompress (`-d`) files
   - `-c` - keeps original files unchanges and writes output on stdout
11. `file stage2`
   - Checking the filetype of stage2
   - stage2 is bzip2 compressed data
12. `bizp2 -dc stage2 > stage3`
13. `file stage3`
   - Checking the filetype of stage3
   - stage3 is bzip2 compressed data
14. `gzip -dc stage3 > stage4`
15. `file stage4`
   - Checking the filetype of stage4
   - stage4 is POSIX tar archive (GNU)
16. `tar -xf stage4`
   - Extracts a file named data5.bin from stage4
   - `tar` - creates archive file (`-cf`) but also allows extraction of these files again (-xf)
17.`file data5.bin`
   - Checking the filetype of data5.bin
   - data5.bin is POSIX tar archive (GNU)
18. `tar -xf data5.bin`
   - Extracts a file named data6.bin from data5.bin
19.`file data6.bin`
   - Checking the filetype of data6.bin
   - data5.bin is bzip2 compressed data
20. `bzip2 -dc data6.bin > stage5`
21. `file stage5`
   - Checking the filetype of stage5
   - stage5 is POSIX tar archive (GNU)
22. `tar -xf stage5`
﻿   - Extracts a file named data8.bin from stage5
23. `file stage5`
   - Checking the filetype of data8.bin
   - data8.bin is gzip compressed data
20. `gzip -dc data8.bin > stage6`
21. `file stage6`
   - Checking the filetype of stage6
   - stage 6 is ASCII text
22. `cat stage6`
   - Prints contents of stage6
23. Password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
