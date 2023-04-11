In Bash, the "uniq" command is used to remove duplicate lines from a sorted file or stream of input.

The basic syntax of the "uniq" command is as follows:

```bash
uniq OPTION... [INPUT [OUTPUT]]
```

Here, "OPTION" is one or more options that specify how to remove duplicates, "INPUT" is an optional argument that specifies the name of the file to read input from, and "OUTPUT" is an optional argument that specifies the name of the file to write output to. If "INPUT" is not specified, uniq will read input from stdin. If "OUTPUT" is not specified, uniq will write output to stdout.

Some common options of the "uniq" command are:

-   "-c" or "--count": This option prefixes each line of output with the number of times that line occurred in the input.
-   "-d" or "--repeated": This option only prints duplicate lines.
-   "-u" or "--unique": This option only prints unique lines.

These are some of the basic options of the "uniq" command. The full list of options can be found in the "uniq" manual page, which can be accessed by typing "man uniq" in a terminal.

By default, the "uniq" command only removes adjacent duplicate lines. If you want to remove all duplicate lines, you can first sort the input using the "sort" command, and then pipe the output to "uniq". For example, the following command will remove all duplicate lines from "file.txt":

```bash
sort file.txt | uniq
```

This will output the sorted lines of "file.txt" with all duplicates removed.