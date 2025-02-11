# Holberton School - I/O Redirections and Filters

This repository contains a series of shell scripts demonstrating input/output redirections and filters in Linux.

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

---

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

This script displays the content of `/etc/passwd`.
```bash
#!/bin/bash
cat /etc/passwd
```

### 3. What about 2?
**File:** `3-twofiles`

This script displays the content of `/etc/passwd` and `/etc/hosts`.
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

This script displays the third line of a file named `iacta`.
```bash
#!/bin/bash
sed -n '3p' iacta
```

### 7. It is a good file that cuts iron without making a noise
**File:** `7-file`

This script creates a file named `\*\'"Best School"\'\*\$\?\*\*\*\*\*\*:)\` containing "Best School".
```bash
#!/bin/bash
echo "Best School" > '\*\'"Best School"\'\*\$\?\*\*\*\*\*\*:)
```

### 8. Save current state of directory
**File:** `8-cwd_state`

This script writes the output of `ls -la` into `ls_cwd_content`.
```bash
#!/bin/bash
ls -la > ls_cwd_content
```

### 9. Duplicate last line
**File:** `9-duplicate_last_line`

This script duplicates the last line of `iacta`.
```bash
#!/bin/bash
tail -n 1 iacta >> iacta
```

### 10. No more javascript
**File:** `10-no_more_js`

This script deletes all JavaScript files (`.js`) in the current directory.
```bash
#!/bin/bash
rm -f *.js
```

### 11. Don't just count your directories, make your directories count
**File:** `11-directories`

This script counts the number of directories in the current directory.
```bash
#!/bin/bash
ls -l | grep "^d" | wc -l
```

### 12. What’s new
**File:** `12-newest_files`

This script lists the 10 newest files in the current directory.
```bash
#!/bin/bash
ls -lt | head -10
```

### 13. Being unique is better than being perfect
**File:** `13-unique`

This script takes a list of words as input and prints only unique words.
```bash
#!/bin/bash
sort | uniq
```

### 14. It must be in that file
**File:** `14-findthatword`

This script finds lines containing the word "Holberton" in the file `test.txt`.
```bash
#!/bin/bash
grep "Holberton" test.txt
```

### 15. Count that word
**File:** `15-countthatword`

This script counts occurrences of "Holberton" in `test.txt`.
```bash
#!/bin/bash
grep -c "Holberton" test.txt
```

### 16. What's next?
**File:** `16-whatsnext`

This script displays lines containing "root" and 3 lines after them in `/etc/passwd`.
```bash
#!/bin/bash
grep -A 3 "root" /etc/passwd
```

### 17. I hate bins
**File:** `17-hidethisword`

This script displays all lines except those containing "bin".
```bash
#!/bin/bash
grep -v "bin" /etc/passwd
```

### 18. Letters only please
**File:** `18-letteronly`

This script displays all lines that contain only letters.
```bash
#!/bin/bash
grep "^[a-zA-Z]*$" /etc/passwd
```

### 19. A to Z
**File:** `19-AZ`

This script replaces all occurrences of `A` and `c` with `Z` and `e`.
```bash
#!/bin/bash
tr 'Ac' 'Ze'
```

### 20. Without C, you would live in hiago
**File:** `20-hiago`

This script removes all occurrences of `c` and `C`.
```bash
#!/bin/bash
tr -d 'cC'
```

### 21. esreveR
**File:** `21-reverse`

This script reverses the input text.
```bash
#!/bin/bash
rev
```

### 22. DJ Cut Killer
**File:** `22-djc`

This script sorts words and displays only those appearing exactly once.
```bash
#!/bin/bash
sort | uniq -u
```

## Usage

Make sure the scripts have execute permissions:
```bash
chmod +x script_name
```
Run the scripts using:
```bash
./script_name
```

---

This repository is part of the Holberton School curriculum.


