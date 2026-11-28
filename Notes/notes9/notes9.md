# Notes 8

## GREP COMMAND (`grep`)

The `grep` command is used to search for specific words, patterns, or text inside files. It helps find information quickly without having to read the entire file.

- **Usage**
  - Used to search for specific words or text inside a file.
  - It can search through one file or multiple files.
  - The `-i` option ignores uppercase and lowercase differences.
  - The `-n` option displays the line number where the matching text is found.
  - The `-r` option searches through files inside directories recursively.
  - It is useful when searching log files, configuration files, and text documents.

- **Formula**
  - `grep pattern filename`
  - `grep -i pattern filename`
  - `grep -n pattern filename`
  - `grep -r pattern directory`

- **Examples**
  - Search for a word in a file:
    - `grep "error" logfile.txt`
  - Search without considering uppercase or lowercase:
    - `grep -i "linux" notes.txt`
  - Display the line number of matching text:
    - `grep -n "error" logfile.txt`
  - Search for a word in all files inside a directory:
    - `grep -r "network" Documents/`
  - Search for a word in a file and display matching lines:
    - `grep "student" names.txt`


## AWK COMMAND (`awk`)

The `awk` command is used to process and analyze text files. It can search for information, select specific fields or columns, and perform calculations. It is especially useful when working with structured text, such as files containing columns separated by spaces.

- **Usage**
  - Used to process and analyze text line by line.
  - It can display specific columns or fields from a file.
  - By default, `awk` separates fields using spaces or tabs.
  - The `$1` represents the first field, `$2` represents the second field, and `$0` represents the entire line.
  - It is useful for extracting information and organizing text data.

- **Formula**
  - `awk '{print $1}' filename`
  - `awk '{print $1, $2}' filename`
  - `awk -F 'delimiter' '{print $field_number}' filename`

- **Examples**
  - Display the first column of a file:
    - `awk '{print $1}' students.txt`
  - Display the first and second columns:
    - `awk '{print $1, $2}' students.txt`
  - Display the entire line:
    - `awk '{print $0}' students.txt`
  - Display the second column of a CSV file:
    - `awk -F ',' '{print $2}' students.csv`
  - Display the first and third columns:
    - `awk '{print $1, $3}' students.txt`



## SED COMMAND (`sed`)

The `sed` command is a stream editor used to search, replace, delete, and modify text in a file or command output. It allows you to make text changes without manually opening a file in a text editor.

- **Usage**
  - Used to search for and replace text.
  - It can delete specific lines from text.
  - It can display selected lines from a file.
  - The `s` command is used for substitution or replacement.
  - It is useful for making quick text changes in files or command output.

- **Formula**
  - `sed 's/old/new/' filename`
  - `sed 's/old/new/g' filename`
  - `sed -n 'line_number p' filename`
  - `sed 'line_number d' filename`

- **Examples**
  - Replace the first occurrence of a word on each line:
    - `sed 's/linux/windows/' notes.txt`
  - Replace all occurrences of a word on each line:
    - `sed 's/linux/windows/g' notes.txt`
  - Display a specific line from a file:
    - `sed -n '5p' notes.txt`
  - Delete a specific line from the output:
    - `sed '3d' notes.txt`
  - Replace a word and save the changes to a new file:
    - `sed 's/old/new/g' notes.txt > updated.txt`



## PIPE COMMAND (`|`)

The pipe (`|`) is used to send the output of one command directly into another command. It allows commands to work together so that the output from the first command becomes the input for the second command.

- **Usage**
  - Used to connect two or more commands together.
  - It sends the output of one command to another command.
  - It helps filter, search, organize, and process information.
  - It is useful because you do not need to create a separate file for every command.

- **Formula**
  - `command1 | command2`
  - `command1 | command2 | command3`

- **Examples**
  - Search for a specific word in the output of a command:
    - `ls -l | grep "txt"`
  - Count the number of files and directories listed:
    - `ls | wc -l`
  - Display the first five lines of command output:
    - `ls -l | head -n 5`
  - Sort the output of a command alphabetically:
    - `ls | sort`
  - Search for a word in the output of another command:
    - `cat notes.txt | grep "Linux"`



## OUTPUT REDIRECTION (`>`)

The output redirection operator (`>`) is used to send the output of a command into a file. If the file already exists, its previous contents are overwritten. If the file does not exist, Linux creates a new file.

- **Usage**
  - Used to save the output of a command into a file.
  - It creates a new file if the file does not already exist.
  - It overwrites the existing contents of a file.
  - It is useful for saving command results for later use.

- **Formula**
  - `command > filename`
  - `command1 > filename`

- **Examples**
  - Save the list of files and directories into a file:
    - `ls > files.txt`
  - Save the contents of a command into a file:
    - `date > date.txt`
  - Save the output of a command into a file:
    - `whoami > username.txt`
  - Save the sorted list of names into a file:
    - `sort names.txt > sorted_names.txt`



## APPEND OUTPUT (`>>`)

The append operator (`>>`) is used to add the output of a command to the end of an existing file. Unlike the `>` operator, it does not erase the existing contents of the file.

- **Usage**
  - Used to add command output to the end of a file.
  - It creates a file if the file does not already exist.
  - It preserves the existing contents of a file.
  - It is useful for keeping records, adding information, and updating log files.

- **Formula**
  - `command >> filename`

- **Examples**
  - Add the current date to a file:
    - `date >> log.txt`
  - Append the list of files to an existing file:
    - `ls >> files.txt`
  - Add the current username to a file:
    - `whoami >> users.txt`
  - Append the output of a command to a log file:
    - `uptime >> system_log.txt`



## QUICK COMMAND REFERENCE

| Command | Purpose |
|---|---|
| `grep` | Search for specific text or patterns in files |
| `awk` | Process text and extract specific fields |
| `sed` | Search, replace, and modify text |
| `\|` | Send output from one command to another |
| `>` | Save command output to a file and overwrite it |
| `>>` | Append command output to the end of a file |
