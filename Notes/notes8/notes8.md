
# Notes 8

## CAT COMMAND (`cat`)
The `cat` command is used to display the contents of a file in the terminal. It can also be used to create files and combine multiple files.

- **Usage**
  - Used to read and display the contents of text files directly in the terminal.
  - It can combine the contents of multiple files into one output.
  - It can also create a new file or add text to an existing file using redirection.
  - It is useful when you want to quickly view or work with file contents without opening a text editor.

- **Formula**
  - `cat filename`
  - `cat > filename`
  - `cat file1 file2`

- **Examples**
  - Display the contents of a file:
    - `cat notes.txt`
  - Display the contents of two files:
    - `cat file1.txt file2.txt`
  - Create a new file:
    - `cat > newfile.txt`
  - Display line numbers:
    - `cat -n notes.txt`

---

## TAC COMMAND (`tac`)

The `tac` command displays the contents of a file in reverse order. It prints the last line first and the first line last.

- **Usage**
  - Used when you want to read a file from the bottom to the top.
  - It displays the last line first and continues upward.
  - It is useful for checking information in reverse order, such as recent entries in a file.

- **Formula**
  - `tac filename`

- **Examples**
  - Display a file in reverse order:
    - `tac notes.txt`
  - Display another file in reverse order:
    - `tac names.txt`
  - Display a file with multiple lines in reverse order:
    - `tac students.txt`

---

## HEAD COMMAND (`head`)

The `head` command displays the first 10 lines of a file by default. It can also display a specific number of lines.

- **Usage**
  - Used to view the beginning of a file without displaying the entire content.
  - By default, it displays the first 10 lines.
  - It is useful when you only need to check the first few lines of a large file.

- **Formula**
  - `head filename`
  - `head -n number filename`

- **Examples**
  - Display the first 10 lines:
    - `head notes.txt`
  - Display the first 5 lines:
    - `head -n 5 notes.txt`
  - Display the first 3 lines:
    - `head -n 3 students.txt`

---

## TAIL COMMAND (`tail`)

The `tail` command displays the last 10 lines of a file by default. It can also display a specific number of lines.

- **Usage**
  - Used to view the last part of a file without displaying all its contents.
  - By default, it displays the last 10 lines.
  - It is useful for checking recent information in log files.
  - The `-f` option allows you to monitor a file and see new lines as they are added.

- **Formula**
  - `tail filename`
  - `tail -n number filename`
  - `tail -f filename`

- **Examples**
  - Display the last 10 lines:
    - `tail notes.txt`
  - Display the last 5 lines:
    - `tail -n 5 notes.txt`
  - Display the last 3 lines:
    - `tail -n 3 students.txt`
  - Continuously monitor a file for new information:
    - `tail -f logfile.txt`

---

## CUT COMMAND (`cut`)

The `cut` command is used to extract specific sections, fields, or characters from each line of a file.

- **Usage**
  - Used to extract specific columns, fields, or characters from lines of text.
  - It is useful when working with organized data, such as CSV files.
  - It allows you to display only the information you need instead of showing the entire line.
  - The `-d` option specifies the delimiter, while the `-f` option selects the field.

- **Formula**
  - `cut -d 'delimiter' -f field_number filename`
  - `cut -c character_range filename`

- **Examples**
  - Display the first field separated by commas:
    - `cut -d ',' -f 1 students.csv`
  - Display the second field separated by commas:
    - `cut -d ',' -f 2 students.csv`
  - Display the first three characters:
    - `cut -c 1-3 names.txt`
  - Display the first and third fields:
    - `cut -d ',' -f 1,3 students.csv`

---

## SORT COMMAND (`sort`)

The `sort` command is used to arrange lines in a file in alphabetical or numerical order. By default, it sorts lines alphabetically.

- **Usage**
  - Used to organize lines of text in alphabetical or numerical order.
  - It is useful for organizing names, numbers, and information stored in text files.
  - The `-r` option sorts in reverse order, and the `-n` option sorts numbers correctly.
  - The `-u` option removes duplicate lines while sorting.

- **Formula**
  - `sort filename`
  - `sort -r filename`
  - `sort -n filename`
  - `sort -u filename`

- **Examples**
  - Sort lines alphabetically:
    - `sort names.txt`
  - Sort lines in reverse alphabetical order:
    - `sort -r names.txt`
  - Sort numbers in numerical order:
    - `sort -n numbers.txt`
  - Sort and save the result in another file:
    - `sort names.txt > sorted.txt`
  - Sort and remove duplicate lines:
    - `sort -u names.txt`

---

## WC COMMAND (`wc`)

The `wc` command is used to count the number of lines, words, and bytes in a file. It helps determine how much content a file contains.

- **Usage**
  - Used to count the amount of information inside a file.
  - It can count lines, words, characters, and bytes.
  - It is useful when you need to check the size or amount of text in a file.
  - Different options allow you to count only specific information, such as lines or words.

- **Formula**
  - `wc filename`
  - `wc -l filename`
  - `wc -w filename`
  - `wc -c filename`
  - `wc -m filename`

- **Examples**
  - Count lines, words, and bytes:
    - `wc notes.txt`
  - Count the number of lines:
    - `wc -l notes.txt`
  - Count the number of words:
    - `wc -w notes.txt`
  - Count the number of bytes:
    - `wc -c notes.txt`
  - Count the number of characters:
    - `wc -m notes.txt`
  - Count the number of lines in multiple files:
    - `wc -l file1.txt file2.txt`

---

## QUICK COMMAND REFERENCE

| Command | Purpose |
|---|---|
| `cat` | Display file contents |
| `tac` | Display file contents in reverse order |
| `head` | Display the beginning of a file |
| `tail` | Display the end of a file |
| `cut` | Extract specific fields or characters |
| `sort` | Arrange lines alphabetically or numerically |
| `wc` | Count lines, words, characters, and bytes |
