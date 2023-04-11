In Bash, the vertical bar symbol "|" and the greater-than symbol ">" have different meanings and functions.

The "|" symbol is known as a [[pipe]], and it is used to connect the output of one command to the input of another command. This allows you to create a chain of commands, where the output of one command is used as the input of the next command. For example, the following command will list all the files in the current directory and then sort them in reverse order by file size:

```bash
ls -l | sort -rn
```

The ">" symbol is known as a [[redirection operator]], and it is used to redirect the output of a command to a file. For example, the following command will create a file named "output.txt" and redirect the output of the "ls" command to that file:

```bash
ls > output.txt
```

In this case, the ">" operator tells Bash to redirect the output of the "ls" command to the "output.txt" file. If the "output.txt" file already exists, it will be overwritten. If you want to append the output of a command to a file instead of overwriting it, you can use the ">>" operator instead of the ">" operator.

So, in summary, the "|" symbol is used to connect the output of one command to the input of another command, while the ">" symbol is used to redirect the output of a command to a file.