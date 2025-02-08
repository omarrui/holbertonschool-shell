# Holberton School - Shell Basics

This repository contains a series of shell scripts designed to help users understand and navigate basic shell commands.

## Table of Contents
1. [0. Where am I?](#0-where-am-i)
2. [1. What’s in there?](#1-whats-in-there)
3. [2. There is no place like home](#2-there-is-no-place-like-home)
4. [3. The long format](#3-the-long-format)
5. [4. Hidden files](#4-hidden-files)
6. [5. I love numbers](#5-i-love-numbers)
7. [6. Welcome](#6-welcome)
8. [7. Betty in my first directory](#7-betty-in-my-first-directory)
9. [8. Bye bye Betty](#8-bye-bye-betty)
10. [9. Bye bye My first directory](#9-bye-bye-my-first-directory)
11. [10. Back to the future](#10-back-to-the-future)
12. [11. Lists](#11-lists)
13. [12. File type](#12-file-type)
14. [13. We are symbols, and inhabit symbols](#13-we-are-symbols-and-inhabit-symbols)
15. [14. Copy HTML files](#14-copy-html-files)
16. [15. Let’s move](#15-lets-move)
17. [16. Clean Emacs](#16-clean-emacs)
18. [17. Tree](#17-tree)

---

## 0. Where am I?
**File:** `0-current_working_directory`

This script prints the absolute path of the current working directory.

```sh
#!/bin/bash
pwd
```

## 1. What’s in there?
**File:** `1-listit`

This script displays the contents of the current directory.

```sh
#!/bin/bash
ls
```

## 2. There is no place like home
**File:** `2-bring_me_home`

This script changes the working directory to the user's home directory without using shell variables.

```sh
#!/bin/bash
cd ~
```

## 3. The long format
**File:** `3-listfiles`

This script lists the contents of the current directory in a long format.

```sh
#!/bin/bash
ls -l
```

## 4. Hidden files
**File:** `4-listmorefiles`

This script lists all files in the current directory, including hidden files, in long format.

```sh
#!/bin/bash
ls -la
```

## 5. I love numbers
**File:** `5-listfilesdigitonly`

This script lists all files, including hidden ones, in long format, with numeric user and group IDs.

```sh
#!/bin/bash
ls -lan
```

## 6. Welcome
**File:** `6-firstdirectory`

This script creates a directory named `my_first_directory` in the `/tmp/` directory.

```sh
#!/bin/bash
mkdir /tmp/my_first_directory
```

## 7. Betty in my first directory
**File:** `7-movethatfile`

This script moves the file `betty` from `/tmp/` to `/tmp/my_first_directory/`.

```sh
#!/bin/bash
mv /tmp/betty /tmp/my_first_directory/
```

## 8. Bye bye Betty
**File:** `8-firstdelete`

This script deletes the file `betty` from `/tmp/my_first_directory/`.

```sh
#!/bin/bash
rm /tmp/my_first_directory/betty
```

## 9. Bye bye My first directory
**File:** `9-firstdirdeletion`

This script deletes the directory `my_first_directory` in `/tmp/`.

```sh
#!/bin/bash
rmdir /tmp/my_first_directory
```

## 10. Back to the future
**File:** `10-back`

This script changes the working directory to the previous one.

```sh
#!/bin/bash
cd -
```

## 11. Lists
**File:** `11-lists`

This script lists all files (including hidden ones) in the current directory, its parent directory, and `/boot`, in long format.

```sh
#!/bin/bash
ls -la . .. /boot
```

## 12. File type
**File:** `12-file_type`

This script prints the type of the file `iamafile`, located in `/tmp/`.

```sh
#!/bin/bash
file /tmp/iamafile
```

## 13. We are symbols, and inhabit symbols
**File:** `13-symbolic_link`

This script creates a symbolic link to `/bin/ls`, named `__ls__`, in the current working directory.

```sh
#!/bin/bash
ln -s /bin/ls __ls__
```

## 14. Copy HTML files
**File:** `14-copy_html`

This script copies all `.html` files from the current directory to its parent, only if they are newer or don't exist in the parent.

```sh
#!/bin/bash
cp -u *.html ../
```

## 15. Let’s move
**File:** `15-lets_move`

This script moves all files starting with an uppercase letter to `/tmp/u`.

```sh
#!/bin/bash
mv [A-Z]* /tmp/u/
```

## 16. Clean Emacs
**File:** `16-clean_emacs`

This script deletes all files in the current directory ending with `~`.

```sh
#!/bin/bash
rm *~
```

## 17. Tree
**File:** `17-tree`

This script creates the directories `welcome/`, `welcome/to/`, and `welcome/to/school/` in the current directory using minimal spaces.

```sh
#!/bin/bash
mkdir -p welcome/to/school
```

---

### Usage
Make sure the scripts have execute permissions:

```sh
chmod +x script_name
```

Run the scripts using:

```sh
./script_name
```


