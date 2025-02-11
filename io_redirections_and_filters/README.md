# Holberton School - I/O Redirections and Filters

This repository contains a series of shell scripts designed to demonstrate and practice input/output redirections and filters in Unix shell.

## Table of Contents

1. Hello World
2. Confused smiley
3. Let's display a file
4. What about 2?
5. Last lines of a file
6. First lines of a file
7. Line #2
8. It is a good file that cuts iron without making a noise
9. Save current state of directory
10. Duplicate last line
11. No more javascript
12. Don't just count your directories, make your directories count
13. What's new
14. It must be in that file
15. Count that word
16. What's next?
17. I hate bins
18. Letters only please
19. A to Z
20. Without C, you would live in hiago
21. esreveR
22. DJ Cut Killer

---

## Script Descriptions

### 1. Hello World
**File:** `0-hello_world`

This script prints "Hello, World" to the standard output.

```bash
#!/bin/bash
echo "Hello, World"
```

### 2. Confused smiley
**File:** `1-confused_smiley`

This script displays a confused smiley: `(Ôo)'.

```bash
#!/bin/bash
echo "(Ôo)'
```

### 3. Let's display a file
**File:** `2-hellofile`

This script displays the content of the `/etc/passwd` file.

```bash
#!/bin/bash
cat /etc/passwd
```

### 4. What about 2?
**File:** `3-twofiles`

This script displays the contents of `/etc/passwd` and `/etc/hosts`.

```bash
#!/bin/bash
cat /etc/passwd /etc/hosts
```

### 5. Last lines of a file
**File:** `4-lastlines`

This script displays the last 10 lines of `/etc/passwd`.

```bash
#!/bin/bash
tail -n 10 /etc/passwd
```

### 6. First lines of a file
**File:** `5-firstlines`

This script displays the first 10 lines of `/etc/passwd`.

```bash
#!/bin/bash
head -n 10 /etc/passwd
```

### 7. Line #2
**File:** `6-third_line`

This script displays the third line of a file named `iacta`.

```bash
#!/bin/bash
sed -n '3p' iacta
```

### 8. It is a good file that cuts iron without making a noise
**File:** `7-cut`

This script extracts and prints the first field (username) from `/etc/passwd`, using `cut`.

```bash
#!/bin/bash
cut -d":" -f1 /etc/passwd
```

### 9. Save current state of directory
**File:** `8-cwd_state`

This script saves the current directory's state into a file named `ls_cwd_content`.

```bash
#!/bin/bash
ls -la > ls_cwd_content
```

### 10. Duplicate last line
**File:** `9-duplicate_last_line`

This script duplicates the last line of a file.

```bash
#!/bin/bash
tail -n 1 file >> file
```

### 11. No more javascript
**File:** `10-no_more_js`

This script removes all files with a `.js` extension in the current directory.

```bash
#!/bin/bash
rm -f *.js
```

### 12. Don't just count your directories, make your directories count
**File:** `11-directories`

This script counts the number of directories (not files) in the current directory.

```bash
#!/bin/bash
ls -l | grep "^d" | wc -l
```

### 13. What's new
**File:** `12-newest_files`

This script displays the 10 newest files in the current directory.

```bash
#!/bin/bash
ls -t | head -n 10
```

### 14. It must be in that file
**File:** `13-unique`

This script prints only unique lines from a file.

```bash
#!/bin/bash
sort file | uniq
```

### 15. Count that word
**File:** `14-findthatword`

This script counts the number of times the word "bin" appears in `/etc/passwd`.

```bash
#!/bin/bash
grep -o "bin" /etc/passwd | wc -l
```

### 16. What's next?
**File:** `15-countpattern`

This script counts the number of lines containing the word "root" in `/etc/passwd`.

```bash
#!/bin/bash
grep -c "root" /etc/passwd
```

### 17. I hate bins
**File:** `16-whatsnext`

This script displays all lines from `/etc/passwd` that do not contain the word "bin".

```bash
#!/bin/bash
grep -v "bin" /etc/passwd
```

### 18. Letters only please
**File:** `17-letteronly`

This script displays all lines from `/etc/passwd` that contain only letters.

```bash
#!/bin/bash
grep "^[a-zA-Z]*$" /etc/passwd
```

### 19. A to Z
**File:** `18-rot13`

This script encodes text using ROT13 encryption.

```bash
#!/bin/bash
tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

### 20. Without C, you would live in hiago
**File:** `19-remove_c`

This script removes all occurrences of the letter "C" (case insensitive) from input.

```bash
#!/bin/bash
tr -d 'cC'
```

### 21. esreveR
**File:** `20-reverse`

This script reverses the input text.

```bash
#!/bin/bash
tac
```

### 22. DJ Cut Killer
**File:** `21-djc`

This script sorts words in `/etc/passwd` and displays only unique ones.

```bash
#!/bin/bash
cut -d":" -f1 /etc/passwd | sort | uniq
```

---

## Usage

Make sure the scripts have execute permissions:

```bash
chmod +x script_name
```

Run the scripts using:

```bash
./script_name
```


