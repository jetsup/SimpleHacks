# Linux Terminal

Running/launching a program from the terminal:

```bash
program-name # if it is accessible globally
./program-name # if the executable is in the current directory
```

Adding a space and an ampersand `&` after program name will launch it in the background.

The programmes launched from terminal will run with their default debug/error message visible.

```bash
program-name > output.txt # write all the program output to a file with filename `output.txt`
program-name > /dev/null # suppress stdout
program-name 2> /dev/null # suppress stderr
program-name > /dev/null 2>&1 # suppress stdout and stderr
```
