An inode (short for index node) is a data structure used in [[Unix]]-based file systems to store information about a file or directory.

Every file and directory on a Unix-based file system is represented by an inode, which contains metadata about the file, such as its owner and permissions, creation and modification times, file size, and the physical location of the data on the disk. The inode number uniquely identifies the file or directory within the file system.

When a file is created, a new inode is also created, which includes information about the file's attributes and location on the disk. As files are modified, their inodes are updated to reflect the changes.

Inodes are important for efficient file system management, as they allow the file system to quickly locate and access files on the disk. They also provide a way for the file system to manage file permissions and ownership, and to handle special file types such as symbolic links and device files.

One important limitation of the inode-based file system is that it can only store a limited number of inodes on a disk. This means that there is a finite number of files that can be stored on a file system, based on the size of the disk and the size of the inodes. Some file systems, such as ext4, use a flexible inode structure to allow for more inodes to be created as needed.