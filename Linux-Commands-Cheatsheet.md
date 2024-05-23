Linux Cheat Sheet

### File System Navigation:

- `cd`: Change directory.
- `ls`: List directory contents.
- `pwd`: Print working directory.
- `mkdir`: Create a directory.
- `rmdir`: Remove a directory.

### File Operations:

- `cp`: Copy files/directories.
- `mv`: Move/rename files/directories.
- `rm`: Remove/delete files/directories.
- `touch`: Create an empty file.
- `cat`: Display file contents.
- `nano`/`vi`: Text editors.
- `sudo find / -name "file*"`: Searches root directory for files with similar name.
- `sudo rm *.png`: Deletes all files with that particular file extension.

### File Permissions:

- `chmod`: Change file permissions.
- `chown`: Change file ownership.

### Process Management:

- `ps`: Display information about active processes.
- `kill`: Terminate processes.

### System Information:

- `uname`: Print system information.
- `df`: Report file system disk space usage.
- `free`: Display amount of free and used memory in the system.

### Package Management:

- `apt`: Advanced Package Tool (Debian/Ubuntu).
- `yum`/`dnf`: Package managers for Red Hat-based distributions.

### Networking:

- `ifconfig`/`ip`: Network interface configuration.
- `ping`: Test network connectivity.
- `ssh`: Secure Shell protocol for secure remote login.

### File Compression/Archiving:

- `tar`: Archive files.
- `gzip`/`gunzip`: Compress/decompress files.
- `zip`/`unzip`: Create/extract ZIP archives.

### Mounting/Unmounting External Drives:

- `mount`: Mount a file system.
- `umount`: Unmount a file system.

### Mounting an External USB Drive:
1. Connect the USB drive to your system.
2. Identify the device name of the USB drive using `lsblk` or `fdisk -l`.
3. Create a mount point using `mkdir`.
4. Mount the USB drive to the mount point using `mount`.

### Backup and Restoration:

- `dd`: Create disk image backups.
  - Example: `sudo dd if=/dev/sdX of=backup_image.img bs=4M` (replace `/dev/sdX` with your device)
- `rsync`: Backup and synchronize files/directories.
  - Example backup: `rsync -av /source/directory /destination/directory`
  - Example restore: `rsync -av /backup/directory /restore/directory`
