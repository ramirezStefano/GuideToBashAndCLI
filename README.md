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

Sure, here are some more commonly used Bash commands:

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
