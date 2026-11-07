# Notes 6

## MKDIR

- **Usage**
  - `mkdir` is used to create new directories (folders).

- **Formula**
  - `mkdir + directory name`

- **Examples**
  - Create a directory named Projects:
    - `mkdir Projects`
  - Create multiple directories:
    - `mkdir Folder1 Folder2`
  - Create a directory and its parent directories:
    - `mkdir -p Documents/School/Notes`

## TOUCH

- **Usage**
  - `touch` is used to create a new empty file. It can also update the timestamp of an existing file.

- **Formula**
  - `touch + file name`

- **Examples**
  - Create a file named notes.txt:
    - `touch notes.txt`
  - Create multiple files:
    - `touch file1.txt file2.txt`
  - Create a file named homework:
    - `touch homework`

## RM

- **Usage**
  - `rm` is used to remove or delete files and directories.

- **Formula**
  - `rm + option + file or directory name`

- **Examples**
  - Delete a file named notes.txt:
    - `rm notes.txt`
  - Delete a file without prompting:
    - `rm -f notes.txt`
  - Delete an empty directory:
    - `rmdir Folder1`
  - Delete a directory and its contents:
    - `rm -r Folder1`

## CP

- **Usage**
  - `cp` is used to copy files and directories from one location to another.

- **Formula**
  - `cp + option + source + destination`

- **Examples**
  - Copy a file named notes.txt:
    - `cp notes.txt backup.txt`
  - Copy a file into the Documents directory:
    - `cp notes.txt Documents/`
  - Copy a directory and its contents:
    - `cp -r Projects Backup`

## MV

- **Usage**
  - `mv` is used to move files and directories from one location to another. It can also rename files and directories.

- **Formula**
  - `mv + source + destination`

- **Examples**
  - Rename a file from old.txt to new.txt:
    - `mv old.txt new.txt`
  - Move a file into the Documents directory:
    - `mv notes.txt Documents/`
  - Move a directory into another directory:
    - `mv Projects Backup/`