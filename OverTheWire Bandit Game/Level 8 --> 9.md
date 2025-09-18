# Level 8 --> 9

## Task 

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Solution 1

1. `ls`
   - Lists the contents of the current directory
2. `sort data.txt | uniq -u`
   - `sort` sorts the lines of a text file aplhabetically and numerically - listing adjacent lines consecutively
   - `uniq` filters **adjacent** matching lines from input and writes to the output
     `-u` only prints unique lines (lines that only appear once)
2. Password - 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

## Solution 2

1. `ls`
   - Lists the contents of the current directory
2. `sort data.txt | uniq -c | grep "1"`
3. - `sort` sorts the lines of a text file aplhabetically and numerically - listing adjacent lines consecutively
   - `uniq` filters **adjacent** matching lines from input and writes to the output
     `-c` prefixes lines by number of occurences
   - `grep "1"` searches for the number 1. There is only one line in the text file which appears once. 
4. Password - 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
