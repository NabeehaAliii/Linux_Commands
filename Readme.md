### Linux Commands Overview

This document provides an overview of various Linux commands discussed, categorized by their functionality. Each command is accompanied by a brief description and usage examples.

## 1. File Management

### `touch`
- **Description**: Creates an empty file or updates the timestamp of an existing file.
- **Usage**:
  ```bash
  touch filename.txt
  ```
  
### `rm`
- **Description**: Removes files or directories.
- **Usage**:
  ```bash
  rm filename.txt        # Removes a file
  rm -r directory_name/  # Removes a directory and its contents
  ```

### `mkdir`
- **Description**: Creates a new directory.
- **Usage**:
  ```bash
  mkdir new_directory
  ```

### `rmdir`
- **Description**: Removes an empty directory.
- **Usage**:
  ```bash
  rmdir empty_directory
  ```

### `cp`
- **Description**: Copies files or directories.
- **Usage**:
  ```bash
  cp source_file destination_file
  cp -r source_directory/ destination_directory/
  ```

### `mv`
- **Description**: Moves or renames files or directories.
- **Usage**:
  ```bash
  mv old_name new_name
  mv file_name /new/path/
  ```

## 2. File Permissions and Ownership

### `chmod`
- **Description**: Changes the file permissions.
- **Usage**:
  ```bash
  chmod 755 filename.txt
  chmod u+x filename.txt  # Adds execute permission for the owner
  ```

### `chown`
- **Description**: Changes the ownership of a file or directory.
- **Usage**:
  ```bash
  chown new_owner filename.txt
  chown new_owner:new_group filename.txt
  ```

### `chgrp`
- **Description**: Changes the group ownership of a file or directory.
- **Usage**:
  ```bash
  chgrp new_group filename.txt
  ```

### `umask`
- **Description**: Sets the default permissions for newly created files and directories.
- **Usage**:
  ```bash
  umask 022
  umask
  ```

## 3. Disk and Filesystem Management

### `mount`
- **Description**: Attaches a filesystem to a specified directory.
- **Usage**:
  ```bash
  sudo mount /dev/sdX1 /mnt
  ```

### `umount`
- **Description**: Detaches a mounted filesystem.
- **Usage**:
  ```bash
  sudo umount /mnt
  ```

### `mountpoint`
- **Description**: Checks if a directory is a mount point.
- **Usage**:
  ```bash
  mountpoint /mnt
  ```

### `df`
- **Description**: Reports disk space usage of mounted filesystems.
- **Usage**:
  ```bash
  df -h
  ```

### `du`
- **Description**: Estimates file and directory disk usage.
- **Usage**:
  ```bash
  du -sh /path/to/directory
  ```

### `lsblk`
- **Description**: Lists information about block devices.
- **Usage**:
  ```bash
  lsblk
  ```

### `fdisk`
- **Description**: A disk partitioning tool.
- **Usage**:
  ```bash
  sudo fdisk /dev/sdX
  ```

## 4. File Compression and Archiving

### `gzip`
- **Description**: Compresses files.
- **Usage**:
  ```bash
  gzip filename.txt
  ```

### `gunzip`
- **Description**: Decompresses files compressed with `gzip`.
- **Usage**:
  ```bash
  gunzip filename.txt.gz
  ```

### `bzip2`
- **Description**: Compresses files using the bzip2 algorithm.
- **Usage**:
  ```bash
  bzip2 filename.txt
  ```

### `bunzip2`
- **Description**: Decompresses files compressed with `bzip2`.
- **Usage**:
  ```bash
  bunzip2 filename.txt.bz2
  ```

### `zip`
- **Description**: Compresses multiple files into a `.zip` archive.
- **Usage**:
  ```bash
  zip archive_name.zip file1 file2 directory/
  ```

### `unzip`
- **Description**: Extracts files from a `.zip` archive.
- **Usage**:
  ```bash
  unzip archive_name.zip
  ```

### `tar`
- **Description**: Creates and extracts `.tar` archives. Often used with compression.
- **Usage**:
  ```bash
  tar -cvf archive_name.tar directory/
  tar -czvf archive_name.tar.gz directory/  # Create a compressed archive
  tar -xvf archive_name.tar                 # Extract an archive
  tar -xzvf archive_name.tar.gz             # Extract a compressed archive
  ```

## 5. User and Group Management

### `adduser`
- **Description**: Adds a new user to the system.
- **Usage**:
  ```bash
  sudo adduser username
  ```

### `useradd`
- **Description**: Adds a new user to the system (basic command with fewer options than `adduser`).
- **Usage**:
  ```bash
  sudo useradd username
  ```

### `usermod`
- **Description**: Modifies a user account.
- **Usage**:
  ```bash
  sudo usermod -aG groupname username
  ```

### `deluser`
- **Description**: Deletes a user account.
- **Usage**:
  ```bash
  sudo deluser username
  ```

### `groupadd`
- **Description**: Adds a new group to the system.
- **Usage**:
  ```bash
  sudo groupadd groupname
  ```

### `groupdel`
- **Description**: Deletes a group from the system.
- **Usage**:
  ```bash
  sudo groupdel groupname
  ```

### `passwd`
- **Description**: Updates a user’s password.
- **Usage**:
  ```bash
  passwd username
  ```

## 6. System Monitoring and Information

### `whoami`
- **Description**: Displays the current logged-in username.
- **Usage**:
  ```bash
  whoami
  ```

### `who`
- **Description**: Shows who is currently logged into the system.
- **Usage**:
  ```bash
  who
  ```

### `w`
- **Description**: Displays who is logged in and what they are doing.
- **Usage**:
  ```bash
  w
  ```

### `ls`
- **Description**: Lists files and directories.
- **Usage**:
  ```bash
  ls -l
  ```

### `pwd`
- **Description**: Displays the current working directory.
- **Usage**:
  ```bash
  pwd
  ```

### `cd`
- **Description**: Changes the current directory.
- **Usage**:
  ```bash
  cd /path/to/directory
  ```

### `ps`
- **Description**: Displays information about running processes.
- **Usage**:
  ```bash
  ps aux
  ```

### `top`
- **Description**: Displays real-time system information and process activity.
- **Usage**:
  ```bash
  top
  ```

### `uname`
- **Description**: Prints system information.
- **Usage**:
  ```bash
  uname -a
  ```

### `which`
- **Description**: Shows the full path of a shell command.
- **Usage**:
  ```bash
  which command_name
  ```

## 7. Other Useful Commands

### `echo`
- **Description**: Outputs text or variables to the terminal.
- **Usage**:
  ```bash
  echo "Hello, World!"
  ```

### `date`
- **Description**: Displays or sets the system date and time.
- **Usage**:
  ```bash
  date
  ```

### `cal`
- **Description**: Displays a calendar.
- **Usage**:
  ```bash
  cal
  ```

### `cat`
- **Description**: Concatenates and displays file content.
- **Usage**:
  ```bash
  cat filename.txt
  ```

### `head`
- **Description**: Displays the first lines of a file.
- **Usage**:
  ```bash
  head -n 10 filename.txt
  ```

### `tail`
- **Description**: Displays the last lines of a file.
- **Usage**:
  ```bash
  tail -n 10 filename.txt
  ```

### `more`
- **Description**: Views file content page by page.
- **Usage**:
  ```bash
  more filename.txt
  ```

### `less`
- **Description**: Views file content with backward movement capability.
- **Usage**:
  ```bash
  less filename.txt
  ```

### `sort`
- **Description**: Sorts lines in a file.
- **Usage**:
  ```bash
  sort filename.txt
  ```

### `wc`
- **Description**: Counts words, lines, and characters in a file.
- **Usage**:
  ```bash
  wc filename.txt


  ```

### `cut`
- **Description**: Removes sections from each line of files.
- **Usage**:
  ```bash
  cut -d ':' -f 1 /etc/passwd
  ```

### `file`
- **Description**: Determines the file type.
- **Usage**:
  ```bash
  file filename.txt
  ```

### `ln`
- **Description**: Creates a hard or symbolic link to a file.
- **Usage**:
  ```bash
  ln source_file link_name
  ln -s source_file link_name  # Symbolic link
  ```

### `pipe` (`|`)
- **Description**: Sends the output of one command as input to another.
- **Usage**:
  ```bash
  command1 | command2
  ```

### `grep`
- **Description**: Searches for patterns within files.
- **Usage**:
  ```bash
  grep "pattern" filename.txt
  ```

### `find`
- **Description**: Searches for files and directories.
- **Usage**:
  ```bash
  find /path -name filename
  ```

### `history`
- **Description**: Displays the command history.
- **Usage**:
  ```bash
  history
  ```

## 8. Session Management

### `su`
- **Description**: Switches to another user.
- **Usage**:
  ```bash
  su - username
  ```

### `sudo`
- **Description**: Executes a command with superuser privileges.
- **Usage**:
  ```bash
  sudo command_name
  ```

### `exit`
- **Description**: Exits the current shell or logged-in user session.
- **Usage**:
  ```bash
  exit
  ```

---

These commands are essential for managing and navigating a Linux environment, whether you're handling files, managing permissions, or monitoring system performance.
```

This `README.md` format provides a structured overview of the commands, making it easy to navigate and understand each command's purpose and usage.
