In Bash, the "cut" command is used to extract columns or fields from a file or stream of input.

The basic syntax of the "cut" command is as follows:

```bash
cut OPTION... [FILE]
```

Here, "OPTION" is one or more options that specify how to extract the fields, and "FILE" is an optional argument that specifies the name of the file to read input from. If "FILE" is not specified, cut will read input from stdin.

Some common options of the "cut" command are:

-   "-c" or "--characters": This option extracts characters from each line of input. You can specify a comma-separated list of character ranges or individual characters. For example, the following command will extract the first five characters from each line of "file.txt":

```bash
cut -c 1-5 file.txt
```

-   "-f" or "--fields": This option extracts fields from each line of input based on a delimiter. You can specify a comma-separated list of field numbers or ranges. By default, the delimiter is a tab, but you can specify a different delimiter using the "-d" option. For example, the following command will extract the second field from each line of "file.txt", assuming that fields are separated by commas:

```bash
cut -f 2 -d ',' file.txt
```

-   "-d" or "--delimiter": This option specifies the delimiter used to separate fields. For example, the following command will extract the second field from each line of "file.txt", assuming that fields are separated by semicolons:

```bash
cut -f 2 -d ';' file.txt
```

These are some of the basic options of the "cut" command. The full list of options can be found in the "cut" manual page, which can be accessed by typing "man cut" in a terminal.