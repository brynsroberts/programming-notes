Linux file permissions control who can access a file and what actions they can perform on it. There are three types of permissions: read (r), write (w), and execute (x), which can be assigned to three categories of users: the owner of the file, the group associated with the file, and all other users.

The permissions are represented by a series of ten characters in the following format:

`-rwxrwxrwx`

The first character is either a dash (-) or a letter that indicates the type of file, such as "d" for a directory or "l" for a symbolic link. The next three characters (rwx) indicate the permissions for the owner, the following three characters indicate the permissions for the group, and the final three characters indicate the permissions for all other users.

Here's what each character in the permissions string means:

-   `r` (read): Allows the user to view the contents of the file
-   `w` (write): Allows the user to modify the contents of the file
-   `x` (execute): Allows the user to execute the file as a program or run it as a script
-   `-` (hyphen): Indicates that a particular permission is not granted

To change file permissions, you can use the [[chmod]] command. For example, to give the owner of a file read, write, and execute permissions, and to give the group and other users only read and execute permissions, you would run the following command:

```bash
chmod 755 filename
```

Here, `7` indicates that the owner has read, write, and execute permissions (4+2+1 = 7), `5` indicates that the group and other users have read and execute permissions (4+1 = 5), and `filename` is the name of the file you want to modify.