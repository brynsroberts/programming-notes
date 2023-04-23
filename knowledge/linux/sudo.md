In [[Linux]], the sudo command allows a user with administrative privileges to execute commands with root privileges. By default, only the root user has access to all system resources and can perform administrative tasks. However, using the sudo command, a regular user can be granted temporary access to perform administrative tasks without having to log in as the root user.

The basic syntax of the sudo command is as follows:

```bash
sudo [command]
```

It's important to note that not all users may have sudo access by default, and it's up to the system administrator to configure which users are allowed to use sudo and what commands they are allowed to run with root privileges. Additionally, running commands with root privileges can be dangerous, as it can cause system instability or security issues, so it's important to use sudo only when necessary and with caution.