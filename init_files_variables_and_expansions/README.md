# Shell Scripting: Variables, Expansions, and Initialization Files

## Learning Objectives
By the end of this project, you should be able to explain:
- What happens when you type `$ ls -l *.txt`
- Shell Initialization Files and their roles
- The difference between local and global variables
- Reserved variables and their roles (e.g., HOME, PATH, PS1)
- Special parameters and `$?`
- Expansions and their usage
- Differences between single and double quotes
- Command substitution using `$()` and backticks
- Performing arithmetic operations in shell
- Creating and managing aliases
- Executing commands from a file in the current shell

---

## Shell Initialization Files
- `/etc/profile`: System-wide environment configurations
- `/etc/profile.d/`: Directory containing scripts sourced by `/etc/profile`
- `~/.bashrc`: User-specific shell initialization file

---

## Variables
### Local vs. Global Variables
- **Local Variables**: Available only in the current shell session
- **Global Variables**: Exported and available to child processes

### Reserved Variables
- `HOME`: User’s home directory
- `PATH`: Directories where the shell searches for commands
- `PS1`: Primary prompt string

### Special Parameters
- `$?`: Exit status of the last executed command

---

## Expansions
- **Tilde Expansion** (`~` for home directory)
- **Brace Expansion** (`{a,b,c}` expands to `a b c`)
- **Parameter Expansion** (`${VAR}`)
- **Command Substitution**
  - Using `$()` (preferred) or backticks `` ` ` ``
- **Arithmetic Expansion** (`$((expression))`)

### Quotes
- **Single Quotes (`'`)**: Literal interpretation
- **Double Quotes (`"`)**: Allows variable expansion

---

## Shell Arithmetic
Perform calculations using:
```bash
$((expression))
```
Example:
```bash
echo $((5 + 3)) # Outputs 8
```

---

## The Alias Command
### Creating an Alias
```bash
alias ls='rm *'
```
### Listing Aliases
```bash
alias
```
### Temporarily Disabling an Alias
```bash
\ls
```

---

## Executing Commands from a File
- `source filename`
- `.` (dot) `filename`

---

## Task Breakdown
### 0. Alias
Create a script that creates an alias `ls` that removes all files:
```bash
#!/bin/bash
alias ls='rm *'
```

### 1. Print Username
```bash
#!/bin/bash
echo "hello $USER"
```

### 2. Modify PATH
```bash
#!/bin/bash
export PATH="$PATH:/action"
```

### 3. Count Directories in PATH
```bash
#!/bin/bash
echo "$PATH" | tr ':' '\n' | wc -l
```

### 4. List Global Variables
```bash
#!/bin/bash
printenv
```

### 5. List Local and Global Variables
```bash
#!/bin/bash
set
```

### 6. Create Local Variable
```bash
#!/bin/bash
BEST="School"
```

### 7. Create Global Variable
```bash
#!/bin/bash
export BEST="School"
```

### 8. Addition
```bash
#!/bin/bash
echo $((128 + TRUEKNOWLEDGE))
```

### 9. Division
```bash
#!/bin/bash
echo $((POWER / DIVIDE))
```

### 10. Exponentiation
```bash
#!/bin/bash
echo $((BREATH ** LOVE))
```

### 11. Base 2 to Base 10 Conversion
- Converts a binary number stored in `$BINARY` to decimal.
```sh
#!/bin/bash
echo $((2#$BINARY))
```

### 12. Print Two-Letter Combinations
- Prints all lowercase letter combinations, except `oo`, using max 64 characters.
```sh
echo {a..z}{a..z} | tr ' ' '\n' | grep -v '^oo$'
```

### 13. Print Floating Point Number
- Prints `$NUM` with two decimal places.
```sh
#!/bin/bash
printf "%.2f\n" "$NUM"
```

### 14. Decimal to Hexadecimal
- Converts a decimal number in `$DECIMAL` to hexadecimal.
```sh
#!/bin/bash
echo "obase=16; $DECIMAL" | bc
```

### 15. Blog Post: `ls *.c`
- Explains step-by-step execution of `ls *.c` in a shell.
- **URL**: [LinkedIn Blog Post](https://www.linkedin.com/posts/rouigui-omar-96514631b_while-learning-about-shell-it-came-across-activity-7295207587438817280-9Y41)

### 16. ROT13 Encryption/Decryption
- Encodes and decodes text using ROT13 cipher.
```sh
#!/bin/bash
tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

### 17. Print Every Other Line
- Prints every alternate line from input, starting with the first.
```sh
#!/bin/bash
paste - - | cut -f1
```

### 18. Add Two Numbers in Custom Bases
- Adds `$WATER` (base `water`) and `$STIR` (base `stir`), outputting in `bestchol`.
```sh
#!/bin/bash
echo $(printf "%o" $((5#$(echo $WATER | tr 'water' '01234') + 5#$(echo $STIR | tr 'stir.' '01234')))) | tr '01234567' 'bestchol'
```

---
This document summarizes key concepts and exercises related to shell scripting.


---

## Requirements
- Scripts must be exactly **two lines** long
- Files must be executable
- First line: `#!/bin/bash`
- README.md explaining each script


