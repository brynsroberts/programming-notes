In Bash, the "sort" command is used to sort lines of text in a file or stream of input.

The basic syntax of the "sort" command is as follows:

```bash
sort OPTION... [FILE]
```

Here, "OPTION" is one or more options that specify how to sort the input, and "FILE" is an optional argument that specifies the name of the file to read input from. If "FILE" is not specified, sort will read input from stdin.

Some common options of the "sort" command are:

-   "-r" or "--reverse": This option sorts the input in reverse order.
-   "-n" or "--numeric-sort": This option sorts the input numerically rather than alphabetically.
-   "-k" or "--key": This option specifies a key to sort by. You can specify a field number or range, as well as a starting and ending character position within each field. For example, the following command will sort "file.txt" by the second field:

```bash
sort -t ',' -k 2 file.txt
```


 Here, the "-t" option specifies the delimiter used to separate fields.

-   "-u" or "--unique": This option removes duplicate lines from the input.
-   "-f" or "--ignore-case": This option sorts the input without regard to case.

These are some of the basic options of the "sort" command. The full list of options can be found in the "sort" manual page, which can be accessed by typing "man sort" in a terminal.

By default, the "sort" command sorts the input alphabetically based on the first character of each line. If you want to sort the input in a different way, you can use the options described above to customize the sorting behavior.