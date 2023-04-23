`apt` is a command-line utility for package management in Debian-based [[Linux]] distributions, such as Ubuntu, Debian, and Linux Mint. It is used to search, install, update, and remove packages and dependencies from the operating system's repositories.

Here are some basic commands to use `apt`:

1.  Update package lists:

```bash
sudo apt update
```

This command updates the local package lists from the repositories, which are databases of available packages.

2.  Install a package:

```bash
sudo apt install [package-name]
```

This command installs a package named `[package-name]` and any dependencies required by it. For example, to install the text editor "nano", you would run:

```bash
sudo apt install nano
```

3.  Remove a package:

```bash
sudo apt remove [package-name]
```

This command removes the specified package and any packages that depend on it but doesn't remove any dependencies that are no longer needed. For example, to remove the "nano" text editor, you would run:

```bash
sudo apt remove nano
```

4.  Purge a package:

```bash
sudo apt purge [package-name]
```

This command removes the specified package, any packages that depend on it, and any configuration files associated with it. For example, to completely remove the "nano" text editor, including its configuration files, you would run:

```bash
sudo apt purge nano
```

5.  Search for a package:

```bash
apt search [package-name]
```

This command searches the repository for packages that match the specified `[package-name]`. For example, to search for a package related to the text editor "nano", you would run:

```bash
apt search nano
```

These are just some of the basic commands for using `apt`. There are many other options and commands available, and you can find more information by using the `man` command or consulting the official documentation.