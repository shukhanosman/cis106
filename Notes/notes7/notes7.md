# Notes 7

## WILDCARDS
- **Usage**
Wildcards are special characters used to match filenames and directories. They make it easier to work with multiple files at once.

- **Formula** 
  - Wildcards are used with Linux commands such as ls, cp, mv, and rm.

- **Examples**
  - List all files ending in .txt:
    - ls *.txt
  - List all files starting with notes:
    - ls notes*
  - List all files:
    - ls *


## ASTERISK (*)
- **Usage**
  - The asterisk matches zero or more characters in a filename.
  
- **Formula**
    -  * + filename pattern
  
- **Examples**
    - List all text files:
        - ls *.txt
    - List all files starting with file:
        - ls file*
    - List all files ending in .pdf:
        - ls *.pdf
  

## QUESTION MARK (?)

- **Usage**
    - The question mark matches exactly one character in a filename.

- **Formula**
    - ? + filename pattern
     
- **Examples**
    - List files with one character after file:
        - ls file?.txt
    - List files with two characters after doc:
        - ls doc??.pdf
    - List files containing one character before .txt:
        - ls ?.txt


## SQUARE BRACKETS ([ ])

- **Usage**
    - Square brackets match exactly one character from a specified group or range of characters.
  
- **Formula**
    - [characters] + filename pattern
  

- **Examples**
  
    - List files named file1, file2, or file3:
        - ls file[123].txt
    - List files containing one lowercase letter:
        - ls file[a-z].txt
    - List files containing one number:
        - ls report[0-9].pdf
  

## NEGATED CHARACTER SET ([! ])


- **Usage**

    - The exclamation mark inside square brackets matches any character that is NOT included in the specified group.


- **Formula**
    - [!characters] + filename pattern
  
- **Examples**

    - List files that do not have 1, 2, or 3 in that position:
        - ls file[!123].txt
    - List files that do not start with the letter a:
        - ls [!a]*.txt


## BRACE EXPANSION ({ })


- **Usage**
    - Brace expansion is used to generate multiple strings, filenames, or directory names with one command.It saves time by allowing multiple directories or files to be created at once.

- **Formula**
    - command + {name1,name2,name3}


- **Examples**

    - Create multiple directories:
        - mkdir {Monday,Tuesday,Wednesday}
    - Create three school subject directories:
        - mkdir {Math,Science,History}
    - Create multiple files:
        - touch file{1,2,3}.txt


## BRACE EXPANSION WITH DIRECTORY STRUCTURES


- **Usage**
    - Brace expansion can be combined with the mkdir -p command to create entire directory structures, including parent and subdirectories.The -p option creates parent directories when they do not already exist.


- **Formula**

    - mkdir -p Parent/{Directory1,Directory2}

- **Examples**
    - Create a School directory with three subdirectories:
        - mkdir -p School/{Math,Science,History}
    - Create two projects with Documents, Images, and Backups directories:
        - mkdir -p Projects/{Project1,Project2}/{Documents,Images,Backups}
    - Create Fall and Spring directories with four weeks each:
        - mkdir -p Classes/{Fall,Spring}/Week{1..4}


## BRACE EXPANSION WITH RANGES


- **Usage**
    - Brace expansion can generate a sequence of numbers or letters.Two dots (..) are used to specify a range.


- **Formula**
{start..end}

- **Examples**

    - Display numbers from 1 to 5:
        - echo {1..5}
    - Display letters from a to e:
        - echo {a..e}
    - Create five numbered files:
        - touch file{1..5}.txt