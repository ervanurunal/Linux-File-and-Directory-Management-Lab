## Linux File and Directory Management Lab

### Overview

This hands-on lab focused on managing files and directories in a Linux environment using the command line.

The lab covered:

* Navigating the Linux file system
* Creating directories
* Creating files
* Copying files and directories
* Moving files and directories
* Renaming files
* Removing files and directories
* Searching file contents
* Editing files using the Nano text editor

These are fundamental Linux skills for IT Support and Cybersecurity roles.

---

### Tools & Resources

#### Tools Used

* Qwiklabs hands-on lab environment
* Linux Virtual Machine
* Linux Shell / Terminal
* Command-Line Interface (CLI)
* `ls`
* `pwd`
* `cd`
* `cat`
* `less`
* `mkdir`
* `rmdir`
* `touch`
* `cp`
* `mv`
* `rm`
* `grep`
* `nano`

#### Lab Type

Hands-on Linux File and Directory Management Lab

#### Operating System

Linux

---

## 1. Linux File System Overview

Linux organizes files and directories in a tree-like structure that begins at the root directory `/`.

Unlike Windows, Linux uses `/` as the root of the file system.

Linux file names are **case-sensitive**.

For example:

```text
File.txt
file.txt
FILE.txt
```

These can represent three different files.

Special characters such as spaces may need to be escaped with a backslash.

Example:

```bash
Europe\ Pictures
```

---

## 2. Linux Navigation Commands

**`ls`**

Displays the contents of the current directory.

---

**`ls -l`**

Displays detailed information about files and directories, including permissions and ownership.

---

**`ls -a`**

Displays hidden files and directories.

---

**`pwd`**

Displays the current working directory.

---

**`cd`**

Changes the current directory.

---

**`cat`**

Displays the contents of a file.

---

**`less`**

Displays large files in a scrollable view.

![practice](https://i.imgur.com/fzCGEiU.png)


---

## 3. Creating Directories

Linux uses the `mkdir` command to create directories.

**Create One Directory**

```bash
mkdir dir_name
```


**Create Multiple Directories**

```bash
mkdir dir1 dir2 dir3
```

![mkdir](https://i.imgur.com/9s7LLJP.png)

---

### Lab Example

Navigate to the Documents directory:

```bash
cd /home/user/Documents
```

View the contents of the `colors` file:

```bash
cat /home/user/Desktop/colors
```

The file contained:

```text
red
blue
green
yellow
magenta
```

Create directories using those names:

```bash
mkdir red blue green yellow magenta
```

Verify:

```bash
ls
```

Expected result:

```text
Hidden  blue  green  magenta  red  yellow
```

![mkdir](https://i.imgur.com/uL7dbMd.png)


---

## 4. Removing Empty Directories

**The `rmdir` command removes empty directories.**

```bash
rmdir dir_name
```

**Multiple directories can also be removed:**

```bash
rmdir dir1 dir2 dir3
```


![rmdir](https://i.imgur.com/jINNlmB.png)

---

## 5. Creating Files

The `touch` command can create an empty file.

```bash
touch empty_file
```

![touch](https://i.imgur.com/kFjx1cG.png)


---

## 6. Copying Files and Directories

The `cp` command is used to copy files or directories.

Basic syntax:

```bash
cp source target
```

---

## 7. Moving and Renaming Files

The `mv` command can be used to:

* Move files
* Move directories
* Rename files
* Rename directories

---

## 8. Working with Spaces in File Names & Moving Files to the Current Directory

Linux requires special handling when a file or directory name contains spaces.

Example:

```text
Europe Pictures
```

You can escape the space with `\`:

```bash
mv Europe\ Pictures /home/user/Pictures
```

![mv](https://i.imgur.com/wjoMcZi.png)

---

## 9. Deleting Files

The `rm` command removes files.

```bash
rm Classical
```

---

## 10. Deleting Directories

To remove an empty directory:

```bash
rmdir Rock
```

---

## 11. Practical File Management Exercise

The lab included a practical exercise involving the `Music` directory.

Navigate to:

```bash
cd /home/user/Music
```

View the directory:

```bash
ls
```

Remove the following files:

```bash
rm Best_of_the_90s 80s_jams Classical
```

Verify:

```bash
ls
```

Then remove the empty `Rock` directory:

```bash
rmdir Rock
```

![rm&rmdir](https://i.imgur.com/mFIxMov.png)

---

## 12. Moving Hidden Files

Linux hidden files usually begin with a period:

```text
.apple
.banana
.broccoli
.milk
```

Navigate to:

```bash
cd /home/user/Pictures
```

Display hidden files:

```bash
ls -a
```

Move the hidden files:

```bash
mv .apple .banana .broccoli .milk /home/user/Documents/Hidden
```

![mv](https://i.imgur.com/mQNJydK.png)

---

## 13. Searching Inside Files with `grep`

`grep` is used to search files for matching text or patterns.

Basic example:

```bash
grep -rw /home/user/Downloads -e "vacation"
```

This searches the Downloads directory for the word:

```text
vacation
```

The lab returned results such as:

```text
/home/user/Downloads/Japan:We enjoyed our vacation here.

/home/user/Downloads/Iceland:We had a great vacation here.
```

The matching directories were then moved:

```bash
mv /home/user/Downloads/Iceland /home/user/Downloads/Japan /home/user/Documents
```

![grep](https://i.imgur.com/xbgnzCi.png)

---

## 14. Commands Cheat Sheet

| Command | Purpose                          |
| ------- | -------------------------------- |
| `ls`    | List directory contents          |
| `ls -l` | List detailed information        |
| `ls -a` | Show hidden files                |
| `pwd`   | Show current directory           |
| `cd`    | Change directory                 |
| `cat`   | Display file contents            |
| `less`  | View large files                 |
| `mkdir` | Create directory                 |
| `rmdir` | Remove empty directory           |
| `touch` | Create empty file                |
| `cp`    | Copy files/directories           |
| `mv`    | Move or rename files/directories |
| `rm`    | Remove files                     |
| `rm -r` | Remove directory and contents    |
| `grep`  | Search inside files              |
| `nano`  | Edit files                       |

---

## 15. IT Support Relevance

These Linux file-management skills are useful for IT Support Specialists because technicians frequently work with:

* Configuration files
* User files
* Application directories
* System directories
* Log files
* Permissions
* File locations
* Troubleshooting data

For example, an IT Support Specialist may need to locate a configuration file, copy it before making changes, modify it, and then verify the result.

A basic workflow might look like:

```text
Locate file
    ↓
View file
    ↓
Create backup/copy
    ↓
Modify file
    ↓
Verify changes
    ↓
Troubleshoot if necessary
```

---

## 16. Cybersecurity Relevance

Linux file-management skills are also important in cybersecurity.

Security professionals may need to:

* Locate suspicious files
* Search directories
* Review configuration files
* Examine logs
* Identify hidden files
* Move investigation artifacts
* Remove malicious or unnecessary files
* Navigate Linux systems during investigations

Commands such as:

```bash
ls
find
grep
cat
less
```

can be useful when investigating files and system activity.

---

## 17. Troubleshooting Scenario

#### Scenario

A user reports that a configuration file contains the word:

```text
security
```

but they don't remember the file name.

#### Possible Approach

Navigate to the appropriate directory:

```bash
cd /path/to/directory
```

Search for the word:

```bash
grep -rw . -e "security"
```

Review the results and identify the file containing the matching text.

This demonstrates how command-line tools can help locate information quickly.

---

## 18. Skills Demonstrated

#### Linux Command Line

* Navigating directories
* Listing files
* Viewing file contents
* Working with hidden files

#### File Management

* Creating files
* Creating directories
* Copying files
* Moving files
* Renaming files
* Deleting files and directories

#### File Search

* Searching file contents with `grep`
* Using search options and flags

#### Text Editing

* Creating files with `touch`
* Editing files with Nano
* Saving and exiting Nano

---
