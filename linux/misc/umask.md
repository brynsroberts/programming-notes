`umask` is a command in Linux and other Unix-like operating systems that is used to set the default [[permissions]] for new files and directories created by a user. The default permissions are determined by subtracting the `umask` value from the maximum permissions (often `777` for directories and `666` for files) and can be thought of as a mask that is applied to the maximum permissions.

The `umask` value is specified as an octal number, with each digit representing the permissions that will be turned off for the new files and directories. The first digit represents the permissions that will be turned off for the owner, the second digit represents the permissions that will be turned off for the group, and the third digit represents the permissions that will be turned off for other users.

For example, if the `umask` value is set to `022`, the default permissions for new files will be `644` (the maximum permissions of `666`, with the `2` in the third digit subtracted), and the default permissions for new directories will be `755` (the maximum permissions of `777`, with the `2` in the third digit subtracted).

To set the `umask` value, you can use the `umask` command followed by the octal value that you want to set. For example, to set the `umask` value to `022`, you would run the following command:

`umask 022`

This will set the `umask` value for the current shell session. If you want to set the `umask` value permanently, you can add the `umask` command to your shell startup file (e.g., `.bashrc` for the Bash shell).

Note that the `umask` value only affects the default permissions for new files and directories created by the user. It does not affect the permissions of existing files and directories, or the permissions set explicitly by the user or administrator.