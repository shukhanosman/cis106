## Notes 3


## What is a graphical user interface (GUI)?
A Graphical User Interface (GUI) is a visual way for users to interact with a computer using graphical elements like windows, icons, menus, and pointers (mice or touchpads). Instead of typing commands, you click, drag, and drop elements to perform tasks.

## What is a desktop environment?
A desktop environment is a collection of graphical software bundles that work together to provide a complete, cohesive GUI experience. It determines the look, feel, and layout of your operating system. It includes the window manager, desktop widgets, file managers, panels, and default applications (like GNOME, KDE Plasma, or XFCE on Linux).

## What is the command line interface (CLI)?
A Command Line Interface (CLI) is a text-based interface used to operate software and operating systems. Instead of clicking icons, users type specific text commands into a prompt, and the system executes them and displays text results.

## How do I access the command line interface (CLI)?
1. From a GUI desktop: Open a program called a terminal emulator (e.g., Terminal, Konsole, iTerm2, or cmd/PowerShell on Windows).

2. Without a GUI: Boot directly into a text-only system or switch to a virtual console.

## What is a virtual console?
A virtual console is a full-screen, text-only user interface provided directly by the Linux/Unix kernel. It operates completely independently of any graphical desktop environment. You can usually switch between different virtual consoles using keyboard shortcuts like Ctrl + Alt + F1 through F6.

## What is a terminal emulator?
A terminal emulator is a graphical application that mimics the behavior of an old-school hardware video terminal. It runs inside your graphical desktop environment, allowing you to access and interact with the command line without leaving your GUI windows.

## What is bash?
Bash (Bourne Again SHell) is a specific shell program and command language. It acts as an interpreter that reads the text commands you type and passes them to the operating system kernel to execute. It is the default shell on many Linux distributions and older macOS systems.

## What is the shell prompt?
The shell prompt is the sequence of characters displayed on the screen indicating that the shell is ready to accept a command. It often displays helpful contextual information, such as your username, the computer's hostname, and your current working directory (e.g., username@hostname:~$).


## clear
* **Definition**:
    * Clears the terminal screen.

* **Usage**: 
    * clear

* **Example**: 
    * clear (wipes all visible text and moves the prompt back to the top left corner).

## echo
* **Definition**: 
    * Prints a line of text or the value of environment variables to the terminal.

* **Usage**: 
    * echo [string_or_variable]

* **Examples**
    * echo "Hello World" (prints "Hello World").
    * echo $USER (prints the username of the currently logged-in user).


## date
* **Definition**: 
    * Displays or sets the system's current date and time.

* **Usage**: 
    * date [options] [+format]

* **Examples**:
    * date (shows current date and time).
    * date "+%Y-%m-%d" (outputs the date formatted as YYYY-MM-DD, like 2026-10-08).

## free
* **Definition**: 
    * Displays the total amount of free and used physical (RAM) and swap memory in the system.

* **Usage**: 
    * free [options]

* **Examples**:
    * uname -a (prints all available system details, including kernel name, version, and architecture).
    * uname -r (prints only the kernel release version).

## uname
* **Definition**: 
    * Prints detailed system and operating system kernel information.

* **Usage**:
    *  uname [options]

* **Examples**:
    * uname -a (prints all available system details, including kernel name, version, and architecture).
    * uname -r (prints only the kernel release version).


## history
* **Definition**: 
    * Displays a numbered list of commands previously executed in the current user session.

* **Usage**: 
    * history [number_of_commands]

* **Examples**:
    * history (prints the entire command history list).
    * history 10 (shows only the last 10 commands executed).
	* !42 (shortcut to re-run the 42nd command in your history list).

## man
* **Definition**: 
    * Opens the built-in system reference manual for any command-line tool.

* **Usage**: 
    * man [command_name]

* **Example**: 
    * man df (opens the comprehensive official manual page explaining how to use df).


## tldr
* **Definition**: 
    * Provides clean, simplified, community-driven "Too Long; Didn't Read" cheat sheets for terminal commands instead of overwhelming manuals.

* **Usage**: t
    * ldr [command_name]

* **Example**: 
    * tldr tar (shows practical, everyday examples of how to zip/unzip files using tar without digging through pages of options).

## cheat
* **Definition**: 
    * An interactive command-line utility that allows you to view and create offline cheat sheets for commands.

* **Usage**: 
    * cheat [command_name]

* **Example**: 
    * cheat curl (presents a quick list of practical copy-pasteable copy examples for using the curl network tool).

## hostname
* **Definition**: 
    * Shows or sets the system's network name.

* **Usage**: 
    * hostname [options]

* **Examples**:
	* hostname (prints the current name of your computer).
	* hostname -I (displays the IP addresses bound to the host).

## df
* **Definition**: 
    * Stands for "disk free"; displays the amount of available and used disk space on all mounted filesystems.

* **Usage**: 
    * df [options]

* **Examples**:
	* df -h (shows disk space in human-readable format like GB or MB).
	*  df -T (includes the filesystem type, like ext4 or xfs, in the output).

## du
* **Definition**: 
    * Stands for "disk usage"; estimates and tracks space used by specific files or directories.

* **Usage**: 
    * du [options] [path]

* **Examples**:
	* du -sh (displays the total summary size of the current directory in human-readable format).
	* du -h /var/log (shows the sizes of all files and subfolders inside the logs directory).


## figlet
* **Definition**:
    * Takes ordinary text and transforms it into large, artistic ASCII banner lettering inside the terminal.

* **Usage**: 
    * figlet [text]

* **Example**: 
    * figlet Hello (outputs the word "Hello" drawn using large block arrangements of text symbols).