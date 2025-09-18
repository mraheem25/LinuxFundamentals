# Level 12 --> 13.md

## Task
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv

# Solution
1. `mktemp -d` gives the pathway for the temporary file to use: `/tmp/tmp.9OLnrxH0Ro`
2. `cp data.txt /tmp/tmp.9OLnrxH0Ro` and then `cd /tmp/tmp.9OLnrxH0Ro`
3. `file data.txt` gives ASCII Text but it is a hexdump
4. `xxd -r data.txt > stage1`: This decompresses the hexdump file and inputs it into a new file `stage1`
5. `file stage1` : gzip compressed data
6. `gzip -dc stage1 > stage2`  This decompresses the gzip file and inputs it into a new file `stage2`
7. `file stage2`: bzip2 compressed data
8. `bizp2 -dc stage2 > stage3`
9. `file stage3`: gzip compressed data
10. `gzip -dc stage3 > stage4`
11. `file stage4`: POSIX tar archive (GNU)
12. `tar -xf stage4`: this generates a new file `data5.bin` which is also a POSIX tar archive file
13. `tar -xf data5.bin`: also generates a new file `data6.bin` which is now bzip2 file
14. `bzip2 -dc data6.bin > stage5`: POSIX tar archive
15. `tar -xf stage5`: generates a `data8.bin` file which is a gzip file
16. `gzip -dc data8.bin > stage6`
17. `file stage6`: ASCII Text
18. `cat stage6`: `The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn`
