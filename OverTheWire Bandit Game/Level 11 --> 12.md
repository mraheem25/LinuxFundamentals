# Level 11 --> 12

## Task 
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

## Solution 1

1. `ls`
   - Lists contents of current working directory
   - `cat data.txt | tr A-Za-z N-ZA-Mn-za-m`
     - `tr` translates characters from one set to another. As the letters have been rotated by 13 positions in the text file, our modified alphabet starts from N and ends at M
       - `A-Z` becomes N-ZA-M
3. Password - 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

## Solution 2 

1. `ls`
   - Lists contents of current working directory
2. `alias ROT13=' tr A-Za-z N-ZA-Mn-za-m'`
   - Sets our translation under the name ROT13
3. `cat data.txt | ROT13`
3. Password - 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
