In Bash, the "wc" command is used to count the number of lines, words, and bytes in a file or stream of input.

The basic syntax of the "wc" command is as follows:

```bash
wc OPTION... [FILE]
```

Here, "OPTION" is one or more options that specify what to count, and "FILE" is an optional argument that specifies the name of the file to read input from. If "FILE" is not specified, wc will read input from stdin.

Some common options of the "wc" command are:

-   "-l" or "--lines": This option counts the number of lines in the input.
-   "-w" or "--words": This option counts the number of words in the input. A word is defined as a sequence of characters separated by whitespace.
-   "-c" or "--bytes": This option counts the number of bytes in the input.
-   "-m" or "--chars": This option counts the number of characters in the input.

These are some of the basic options of the "wc" command. The full list of options can be found in the "wc" manual page, which can be accessed by typing "man wc" in a terminal.

If you specify multiple options, wc will count all of the specified items. For example, the following command will count the number of lines, words, and bytes in "file.txt":

```bash
wc -l -w -c file.txt
```

This will output three numbers: the number of lines, the number of words, and the number of bytes, respectively.