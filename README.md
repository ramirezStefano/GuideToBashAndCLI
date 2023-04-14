# Starter Guide To Bash And CLI

## Objective

This is a repo for all people looking to learn or expand some of the most used 'bash' functions that are used and/or can be used to move smoothly in the CLI(command line interface) e.g. terminal in OSX or a version of bash.

## The man and help.

If we want some insight on a CLI program usage we can run the command:

```shell
man <program>
```

Such a command will output the program manual.

Sometimes a manual is not provided by the program, but fear not for there there are usually help functions in the program or both! so:

```shell
<program> -help
```

or

```shell
<program> --help
```

or just typing the name of the program can lead to some sort of clue as to how to get the program usage and options.

---

## Directory

Everything is a file or a directory in the most simplest of ways. If we want to know where we are currently in the CLI we can type:

```shell
pwd
```

this stands for print working directory.

---

To get a listing of what's in the directory we can run the command:

```shell
ls
```

this command lists everything that is in the current working direcotry or '.'

Try:

```shell
man ls
```

And enjoy the beauty of the ls manual.

press q to quit.

---

To switch to another directory we use the command:

```shell
cd
```

that stands for **change directory** and the ellipsis for the directory that we want to move or change into. (same as clicking the folder in the GUI of our finder or regular window)

the '.' in the terminal has the value of the current directory, the '..' has the value of the parent of previous directory. e.g.:

```shell
cd ..
```

This will take us to the 'folder' or directory that houses the current dir, like clicking the back in the GUI to got to the folder before.

To be continued....
