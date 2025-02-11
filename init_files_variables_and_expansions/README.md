Shell, init files, variables and expansions
Amateur
By: Julien Barbier

Description
This project consists of a series of shell scripts that demonstrate basic shell commands, handling of shell initialization files, variables, expansions, and arithmetic. Each script is exactly two lines long (the first line is always exactly #!/bin/bash), ends with a new line, and adheres to strict constraints.

Requirements
Allowed editors: vi, vim, emacs
Tested on: Ubuntu 20.04 LTS
Script constraints:
Each script must be exactly two lines long (use wc -l filename to verify it prints 2).
Each file must end with a new line.
The first line must be exactly:
sh
Copy
Edit
#!/bin/bash
Forbidden: You are not allowed to use &&, || or ;, nor may you use bc, sed or awk.
All files must be executable.
Resources
Read or watch:
Expansions
Shell Arithmetic
Variables
Shell initialization files
The alias Command
Technical Writing
Man pages or help for: printenv, set, unset, export, alias, unalias, ., source, printf
Learning Objectives
At the end of this project you should be able to explain to anyone (without help from Google):

What happens when you type ls -l *.txt
The roles of /etc/profile, /etc/profile.d, and ~/.bashrc
The difference between local and global variables, and what reserved variables are
How to create, update, and delete shell variables
The roles of reserved variables like HOME, PATH, and PS1
What special parameters are (e.g., $?)
How expansions work and the difference between single and double quotes
How command substitution works using $() and backticks
How to perform arithmetic operations in the shell
How to create and manage aliases
How to execute commands from a file in the current shell
Tasks
0. <o>
Task: Create a script that creates an alias.

Alias Name: ls
Alias Value: rm *
Usage: After sourcing this script, running ls will effectively call rm * (so use the escaped \ls to bypass it).
sh
Copy
Edit
#!/bin/bash
alias ls='rm *'
1. Hello you
Task: Create a script that prints hello user, where user is the current Linux user.

sh
Copy
Edit
#!/bin/bash
echo "hello $USER"
2. The path to success is to take massive, determined action
Task: Add /action to the PATH so that it’s the last directory searched.

sh
Copy
Edit
#!/bin/bash
export PATH="$PATH:/action"
3. If the path be beautiful, let us not ask where it leads
Task: Create a script that counts the number of directories in the PATH.

sh
Copy
Edit
#!/bin/bash
echo "$PATH" | tr ':' '\n' | wc -l
4. Global variables
Task: Create a script that lists all environment variables.

sh
Copy
Edit
#!/bin/bash
printenv
5. Local variables
Task: Create a script that lists all local variables, environment variables, and functions.

sh
Copy
Edit
#!/bin/bash
set
6. Local variable
Task: Create a script that creates a new local variable.

Variable Name: BEST
Value: School
sh
Copy
Edit
#!/bin/bash
BEST="School"
7. Global variable
Task: Create a script that creates a new global variable.

Variable Name: BEST
Value: School
sh
Copy
Edit
#!/bin/bash
export BEST="School"
8. Every addition to true knowledge is an addition to human power
Task: Create a script that prints the result of adding 128 to the value stored in the environment variable TRUEKNOWLEDGE.

sh
Copy
Edit
#!/bin/bash
echo $((128 + TRUEKNOWLEDGE))
9. Divide and rule
Task: Create a script that prints the result of dividing the environment variable POWER by DIVIDE.

sh
Copy
Edit
#!/bin/bash
echo $((POWER / DIVIDE))
10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath
Task: Create a script that displays the result of raising BREATH to the power of LOVE.

sh
Copy
Edit
#!/bin/bash
echo $((BREATH ** LOVE))
11. There are 10 types of people in the world -- Those who understand binary, and those who don't
Task: Create a script that converts a binary number (stored in the environment variable BINARY) to decimal.

sh
Copy
Edit
#!/bin/bash
echo $((2#$BINARY))
12. Combination
Task: Create a script that prints all possible combinations of two letters (lowercase, from a to z), except for oo.

Details:
One combination per line
Output should be alphabetically ordered, starting with aa
Do not print oo
The script must contain a maximum of 64 characters
sh
Copy
Edit
#!/bin/bash
echo {a..z}{a..z} | tr ' ' '\n' | grep -v '^oo$'
13. Floats
Task: Create a script that prints the value of NUM with two decimal places.

sh
Copy
Edit
#!/bin/bash
printf "%.2f\n" "$NUM"
14. Decimal to Hexadecimal
Task: Create a script that converts a decimal number (stored in the environment variable DECIMAL) to hexadecimal.

sh
Copy
Edit
#!/bin/bash
printf "%x\n" "$DECIMAL"
15. What happens when you type ls *.c
Advanced Task:
Write a blog post describing, step by step, what happens when you type ls *.c and hit Enter. Explain every step (e.g., globbing, expansion, command execution) so that even a beginner understands.

Requirements:
Include at least one picture at the top of your blog post
Publish your post on Medium or LinkedIn
Share the URL(s) below
URL:
LinkedIn Blog Post
16. Everyone is a proponent of strong encryption
Task: Create a script that encodes and decodes text using ROT13 encryption (assume ASCII).

sh
Copy
Edit
#!/bin/bash
tr 'A-Za-z' 'N-ZA-Mn-za-m'
17. The eggs of the brood need to be an odd number
Task: Create a script that prints every other line from the input (i.e., odd-numbered lines), starting with the first line.

Compliant Solution: Uses paste and cut (avoiding forbidden commands).
sh
Copy
Edit
#!/bin/bash
paste - - | cut -f1
18. I'm an instant star. Just add water and stir.
Task: Create a script that adds the two numbers stored in the environment variables WATER and STIR and prints the result.

Details:
WATER is in base water
STIR is in base stir
The result should be printed in base bestchol
Example:
sh
Copy
Edit
export WATER="ewwatratewa"
export STIR="ti.itirtrtr"
./17-water_and_stir  # Expected output: shtbeolhc
sh
Copy
Edit
#!/bin/bash
echo "$(echo $(( $(echo "$WATER" | tr 'water' '01234') + $(echo "$STIR" | tr 'stir.' '01234') )) | tr '0123456789' 'shtbeolhc')"

