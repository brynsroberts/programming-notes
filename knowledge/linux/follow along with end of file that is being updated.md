To display the end of a log file, you can use the "[[tail]]" command with the "-f" option to follow the file as it updates in real time. Here's an example:

```bash
tail -f /var/log/apache2/access.log
```

This command will display the last 10 lines of the "access.log" file and continuously update the output as new entries are added to the file. You can adjust the number of lines displayed with the "-n" option, like this:

```bash
tail -f /var/log/apache2/access.log -n 50

```

This command will display the last 50 lines of the file. If you want to view the end of the file without following updates in real time, you can use the "tail" command without the "-f" option:

```bash
tail /var/log/apache2/access.log
```

This command will display the last 10 lines of the file and exit. Again, you can adjust the number of lines displayed with the "-n" option.