The `du` command in [[Bash]] is a utility that stands for "disk usage". It is used to estimate the space used by files and directories on a file system.

When you run the `du` command, it displays the space used by a file or directory and any subdirectories it contains. By default, `du` displays the space used in kilobytes (KB), but you can use the `-h` option to display the space used in human-readable format (e.g., KB, MB, GB).

Here's an example of how to use the `du` command:

```bash
du myfile.txt 4   
```

In this example, the `du` command displays the size of `myfile.txt` in kilobytes. The `4` indicates that the file uses 4 kilobytes of disk space.

You can also use the `du` command with various options and arguments to customize its behavior. For example, you can use the `-s` option to display only the total space used by a file or directory, without listing the sizes of individual files.