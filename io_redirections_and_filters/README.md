# Holberton School - I/O Redirections and Filters

This repository contains a series of shell scripts demonstrating various I/O redirections and filters.

## Table of Contents

0. Hello World  
1. Confused smiley  
2. Let's display a file  
3. What about 2?  
4. Last lines of a file  
5. I'd prefer the first ones actually  
6. Line #2  
7. It is a good file that cuts iron without making a noise  
8. Save current state of directory  
9. Duplicate last line  
10. No more javascript  
11. Don't just count your directories, make your directories count  
12. What’s new  
13. Being unique is better than being perfect  
14. It must be in that file  
15. Count that word  
16. What's next?  
17. I hate bins  
18. Letters only please  
19. A to Z  
20. Without C, you would live in hiago  
21. esreveR  
22. DJ Cut Killer  

## Script Descriptions

### 0. Hello World
**File:** `0-hello_world`

This script prints "Hello, World" to standard output.

```bash
#!/bin/bash
echo "Hello, World"
```

### 1. Confused smiley
**File:** `1-confused_smiley`

This script displays a confused smiley `"(Ôo)"`.

```bash
#!/bin/bash
echo "(Ôo)"
```

### 2. Let's display a file
**File:** `2-hellofile`

This script displays the contents of `/etc/passwd`.

```bash
#!/bin/bash
cat /etc/passwd
```

### 3. What about 2?
**File:** `3-twofiles`

This script displays the contents of `/etc/passwd` and `/etc/hosts`.

```bash
#!/bin/bash
cat /etc/passwd /etc/hosts
```

### 4. Last lines of a file
**File:** `4-lastlines`

This script displays the last 10 lines of `/etc/passwd`.

```bash
#!/bin/bash
tail /etc/passwd
```

### 5. I'd prefer the first ones actually
**File:** `5-firstlines`

This script displays the first 10 lines of `/etc/passwd`.

```bash
#!/bin/bash
head /etc/passwd
```

### 6. Line #2
**File:** `6-third_line`

This script displays the third line of the file `iacta`.

```bash
#!/bin/bash
head -3 iacta | tail -1
```

### 7. It is a good file that cuts iron without making a noise
**File:** `7-file`

This script creates a file named `\*\'Best School\'\*$?\*\*\*\*\*:)", containing the text `Best School`.

```bash
#!/bin/bash
echo -e "Best School"  >> "\\*\\\\'\"Best School\"\\'\\\\*$\\?\\*\\*\\*\\*\\*:)"
```

### 8. Save current state of directory
**File:** `8-cwd_state`

This script writes the result of `ls -la` into the file `ls_cwd_content`.

```bash
#!/bin/bash
ls -la > ls_cwd_content
```

### 9. Duplicate last line
**File:** `9-duplicate_last_line`

This script duplicates the last line of a file.

```bash
#!/bin/bash
tail -1 iacta >> iacta
```

### 10. No more javascript
**File:** `10-no_more_js`

This script deletes all `.js` files in the current directory.

```bash
#!/bin/bash
rm -f *.js
```

### 11. Don't just count your directories, make your directories count
**File:** `11-directories`

This script counts the number of directories (excluding files) in the current directory.

```bash
#!/bin/bash
find . -type d | wc -l
```

### 12. What’s new
**File:** `12-newest_files`

This script displays the 10 newest files in the current directory.

```bash
#!/bin/bash
ls -lt | head -10
```

### 13. Being unique is better than being perfect
**File:** `13-unique`

This script finds and removes duplicate lines in a file.

```bash
#!/bin/bash
sort file | uniq
```

### 14. It must be in that file
**File:** `14-findthatword`

This script finds lines containing "root" in `/etc/passwd`.

```bash
#!/bin/bash
grep "root" /etc/passwd
```

### 15. Count that word
**File:** `15-countthatword`

This script counts occurrences of "bin" in `/etc/passwd`.

```bash
#!/bin/bash
grep -c "bin" /etc/passwd
```

### 16. What's next?
**File:** `16-whatsnext`

This script finds lines containing "root" in `/etc/passwd`, ignoring case.

```bash
#!/bin/bash
grep -i "root" /etc/passwd
```

### 17. I hate bins
**File:** `17-hatebins`

This script displays all lines in `/etc/passwd` that do **not** contain "bin".

```bash
#!/bin/bash
grep -v "bin" /etc/passwd
```

### 18. Letters only please
**File:** `18-lettersonly`

This script displays only lines that contain letters (ignoring digits).

```bash
#!/bin/bash
grep "[a-zA-Z]" /etc/passwd
```

### 19. A to Z
**File:** `19-AtoZ`

This script replaces all occurrences of `A` and `Z` in a file.

```bash
#!/bin/bash
tr 'A' 'Z' < file
```

### 20. Without C, you would live in hiago
**File:** `20-withoutc`

This script removes all occurrences of the letter `c` from input.

```bash
#!/bin/bash
tr -d 'c'
```

### 21. esreveR
**File:** `21-reverse`

This script reverses the content of a file.

```bash
#!/bin/bash
tac file
```

### 22. DJ Cut Killer
**File:** `22-djcutkiller`

This script sorts words in a file and displays them.

```bash
#!/bin/bash
sort file
```

## Usage
Ensure the scripts have execution permissions:

```bash
chmod +x script_name
```

Run the scripts using:

```bash
./script_name
```

