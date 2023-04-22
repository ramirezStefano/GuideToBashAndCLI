# Bash Commands

## Navigation

| Command          | Description                                           |
| ---------------- | ----------------------------------------------------- |
| `cd [directory]` | Change the current working directory to `[directory]` |
| `pwd`            | Print the current working directory                   |
| `ls`             | List the contents of the current directory            |
| `ls [directory]` | List the contents of `[directory]`                    |

## Manipulating Files and Directories

| Command                     | Description                                |
| --------------------------- | ------------------------------------------ |
| `mkdir [directory]`         | Create a new directory named `[directory]` |
| `touch [filename]`          | Create a new file named `[filename]`       |
| `cp [source] [destination]` | Copy `[source]` to `[destination]`         |
| `mv [source] [destination]` | Move `[source]` to `[destination]`         |
| `rm [file]`                 | Remove `[file]`                            |
| `rm -r [directory]`         | Remove `[directory]` and its contents      |

## Input and Output

| Command          | Description                                         |
| ---------------- | --------------------------------------------------- |
| `echo [message]` | Print `[message]` to the console                    |
| `cat [file]`     | Print the contents of `[file]` to the console       |
| `head [file]`    | Print the first 10 lines of `[file]` to the console |
| `tail [file]`    | Print the last 10 lines of `[file]` to the console  |

## Searching

| Command                         | Description                                                       |
| ------------------------------- | ----------------------------------------------------------------- |
| `grep [pattern] [file]`         | Search `[file]` for lines containing `[pattern]`                  |
| `grep -r [pattern] [directory]` | Recursively search `[directory]` for files containing `[pattern]` |

## Permissions

| Command                | Description                                    |
| ---------------------- | ---------------------------------------------- |
| `chmod [mode] [file]`  | Change the permissions of `[file]` to `[mode]` |
| `chown [user] [file]`  | Change the owner of `[file]` to `[user]`       |
| `chgrp [group] [file]` | Change the group of `[file]` to `[group]`      |

## System Information

| Command    | Description                        |
| ---------- | ---------------------------------- |
| `whoami`   | Print the current user's username  |
| `hostname` | Print the name of the current host |
| `uptime`   | Print the system uptime            |

## Process Management

| Command                  | Description                                                        |
| ------------------------ | ------------------------------------------------------------------ |
| `ps`                     | List the currently running processes                               |
| `ps aux`                 | List all running processes and their details                       |
| `kill [process_id]`      | Send a signal to stop the process with `[process_id]`              |
| `killall [process_name]` | Send a signal to stop all processes with the name `[process_name]` |

## Networking

| Command             | Description                                                                         |
| ------------------- | ----------------------------------------------------------------------------------- |
| `ping [host]`       | Test the connectivity to `[host]` by sending ICMP echo request packets              |
| `traceroute [host]` | Show the path taken by packets to reach `[host]`                                    |
| `wget [url]`        | Download a file from `[url]`                                                        |
| `curl [url]`        | Transfer data from or to a server using various protocols including HTTP, FTP, etc. |

## System Maintenance

| Command          | Description                                                           |
| ---------------- | --------------------------------------------------------------------- |
| `df`             | Show the amount of free disk space on each mounted filesystem         |
| `du [directory]` | Show the disk usage of the files and directories within `[directory]` |
| `top`            | Display the system's processes in real time                           |
| `history`        | Show a list of commands previously executed by the user               |

## User Management

| Command              | Description                                                             |
| -------------------- | ----------------------------------------------------------------------- |
| `useradd [username]` | Create a new user account with the username `[username]`                |
| `userdel [username]` | Delete the user account with the username `[username]`                  |
| `passwd [username]`  | Change the password for the user account with the username `[username]` |
| `su [username]`      | Switch to the user account with the username `[username]`               |

## Miscellaneous

| Command | Description                              |
| ------- | ---------------------------------------- |
| `date`  | Display the current date and time        |
| `cal`   | Display a calendar for the current month |
| `clear` | Clear the terminal screen                |
| `exit`  | Exit the current terminal session        |

These are just some of the most commonly used Bash commands, but there are many more. It's worth noting that most of these commands have additional options and arguments that can be used to customize their behavior, and you can find more information about them in the Bash manual or by using the `man` command followed by the name of the command.

Certainly! Here's a summary of piping in Bash:

# Piping in Bash

Piping is a powerful feature in Bash that allows you to take the output of one command and use it as the input for another command. This allows you to chain together multiple commands to perform more complex operations.

## Syntax

To pipe the output of one command to the input of another command, you use the `|` character. For example:

```
command1 | command2
```

In this syntax, `command1` produces output, which is then passed as input to `command2`.

## Examples

Here are some examples of piping in Bash:

### Example 1: Counting files

To count the number of files in the current directory, you could use the following command:

```
ls | wc -l
```

In this command, `ls` lists all the files in the current directory, and the output is piped to the `wc` command, which counts the number of lines in the input.

### Example 2: Searching for files

To search for all files in the current directory that contain the word "hello", you could use the following command:

```
ls | grep hello
```

In this command, the output of `ls` is piped to the `grep` command, which searches for the word "hello" in the input and returns any lines that contain the word "hello".

### Example 3: Chaining commands

You can chain together any number of commands using piping. For example, you could search for all files in the current directory that contain the word "hello", count the number of lines that contain the word "hello", and then sort the output by the number of lines using the `sort` command like this:

```
ls | grep hello | wc -l | sort
```

In this command, the output of `ls` is piped to the `grep` command, which searches for the word "hello" in the input. The output of `grep` is then piped to the `wc` command, which counts the number of lines that contain the word "hello". Finally, the output of `wc` is piped to the `sort` command, which sorts the output by the number of lines.

By mastering piping, you can become much more efficient and productive on the command line.

# Vim

Vim is a powerful text editor that is included with most Unix-based operating systems, including Linux and macOS. It is designed to be used in a terminal window and provides a wide range of features for editing text, including syntax highlighting, code folding, and macro recording.

## Basic Usage

To open a file in Vim, you simply type the `vim` command followed by the name of the file you want to edit. For example:

```
vim example.txt
```

Once the file is open, you can use a wide range of commands to edit the text. Some basic commands include:

- `i` to enter insert mode, where you can type new text
- `Esc` to exit insert mode and return to command mode
- `:w` to save the changes you've made to the file
- `:q` to quit Vim
- `:wq` to save the changes and quit Vim

## Advanced Features

Vim has many advanced features that can help you edit text more efficiently. For example:

- Macros: You can record a series of keystrokes as a macro and then play it back to repeat the same series of commands on multiple lines of text.
- Plugins: Vim has a wide range of plugins that you can use to add new features to the editor, such as code completion, file browsing, and syntax checking.
- Customization: Vim is highly customizable, and you can configure it to work the way you want by editing the `vimrc` file.

# Emacs

Emacs is another powerful text editor that is widely used in the Unix/Linux world. Like Vim, it is designed to be used in a terminal window, but it also has a graphical user interface (GUI) version that can be run on most operating systems.

## Basic Usage

To open a file in Emacs, you simply type the `emacs` command followed by the name of the file you want to edit. For example:

```
emacs example.txt
```

Once the file is open, you can use a wide range of commands to edit the text. Some basic commands include:

- `Ctrl + x, Ctrl + s` to save the changes you've made to the file
- `Ctrl + x, Ctrl + c` to quit Emacs
- `Ctrl + g` to cancel the current command or operation
- `Ctrl + x, Ctrl + f` to open a new file for editing
- `Ctrl + x, Ctrl + b` to switch between open files

## Advanced Features

Emacs has many advanced features that can help you edit text more efficiently. For example:

- Macros: You can record a series of keystrokes as a macro and then play it back to repeat the same series of commands on multiple lines of text.
- Modes: Emacs has modes for editing specific types of files, such as programming languages or markup languages. These modes provide syntax highlighting and other features specific to the language or format.
- Plugins: Emacs has a wide range of plugins that you can use to add new features to the editor, such as code completion, version control integration, and file browsing.
- Customization: Like Vim, Emacs is highly customizable, and you can configure it to work the way you want by editing the `.emacs` file.

# The `>>` Tool

The `>>` tool is a Bash command that appends the output of a command to the end of a file. Here's an example:

```
echo "Hello, world!" >> example.txt
```

In this command, the `echo` command outputs the text "Hello, world!" to the terminal window, and the `>>` tool appends the output to the end of the file `example.txt`. If the file doesn't exist, the `>>` tool creates it.

You can use the `>>` tool with any command that produces output. For example, you could use it with the `ls` command to append a list of files in the current directory to a file:

```
ls >> filelist.txt
```

In this command, the output of `ls` (a list of files in the current directory) is appended to the end of the file `filelist.txt`.

# Regular Expressions (Regex) 101

Regular expressions, also known as regex, are a powerful tool for working with text. A regular expression is a pattern of characters that describes a set of strings. For example, the regular expression `hello` matches the strings "hello", "Hello", and "heLLo".

## Basic Syntax

Regular expressions are composed of characters that match specific patterns of text. Here are some examples of basic syntax:

- `.`: Matches any single character
- `[ ]`: Matches any one of the characters in the brackets
- `[^ ]`: Matches any character not in the brackets
- `*`: Matches zero or more occurrences of the previous character
- `+`: Matches one or more occurrences of the previous character
- `?`: Matches zero or one occurrence of the previous character
- `|`: Matches either the expression on the left or the expression on the right

For example, the regular expression `b[aeiou]t` matches the strings "bat", "bet", "bit", "bot", and "but".

## Advanced Syntax

Regular expressions can also include more advanced syntax to match more complex patterns. Here are some examples:

- `^`: Matches the beginning of a line
- `$`: Matches the end of a line
- `()` and `|`: Matches groups of characters and allows you to specify alternatives within the group. For example, the regular expression `(cat|dog)` matches the strings "cat" and "dog".
- `\`: Escapes special characters so they are treated as literal characters. For example, the regular expression `\.` matches a period.

## Practical Uses

Regular expressions are used in many different programming languages and tools, including Bash, Python, Perl, and more. Some common uses for regular expressions include:

- Validating input: Regular expressions can be used to ensure that user input matches a specific pattern. For example, you could use a regular expression to validate an email address or a phone number.
- Searching and replacing: Regular expressions can be used to search for specific patterns of text and replace them with other text. For example, you could use a regular expression to replace all occurrences of a word in a document.
- Extracting information: Regular expressions can be used to extract specific pieces of information from a larger text. For example, you could use a regular expression to extract all of the email addresses from a file.

Overall, regular expressions are a powerful tool for working with text, and they can be used to solve many different problems.
