# Holberton School - Shell Permissions

This repository contains a series of shell scripts designed to help users understand and manipulate file permissions in a Unix-based system.

## Table of Contents

0. My name is Betty  
1. Who am I  
2. Groups  
3. New owner  
4. Empty!  
5. Execute  
6. Multiple permissions  
7. Everybody!  
8. James Bond  
9. John Doe  
10. Look in the mirror  
11. Directories  
12. More directories  
13. Change group  
14. Owner and group  
15. Symbolic links  
16. If only  

---

### 0. My name is Betty  
**File:** `0-iam_betty`  
This script changes the current user to `betty`.

```bash
#!/bin/bash
su betty
```

### 1. Who am I  
**File:** `1-who_am_i`  
This script prints the effective username of the current user.

```bash
#!/bin/bash
whoami
```

### 2. Groups  
**File:** `2-groups`  
This script prints all the groups the current user is part of.

```bash
#!/bin/bash
groups
```

### 3. New owner  
**File:** `3-new_owner`  
This script changes the owner of the file `hello` to `betty`.

```bash
#!/bin/bash
chown betty hello
```

### 4. Empty!  
**File:** `4-empty`  
This script creates an empty file named `hello`.

```bash
#!/bin/bash
touch hello
```

### 5. Execute  
**File:** `5-execute`  
This script adds execute permission to the owner of the file `hello`.

```bash
#!/bin/bash
chmod u+x hello
```

### 6. Multiple permissions  
**File:** `6-multiple_permissions`  
This script adds execute permission to the owner and group, and read permission to others for the file `hello`.

```bash
#!/bin/bash
chmod ug+x,o+r hello
```

### 7. Everybody!  
**File:** `7-everybody`  
This script grants execution permission to everyone for the file `hello`.

```bash
#!/bin/bash
chmod a+x hello
```

### 8. James Bond  
**File:** `8-James_Bond`  
This script sets `hello`'s permissions so that only others have all permissions.

```bash
#!/bin/bash
chmod 007 hello
```

### 9. John Doe  
**File:** `9-John_Doe`  
This script sets the permissions of `hello` to `rwxr-x-wx`.

```bash
#!/bin/bash
chmod 753 hello
```

### 10. Look in the mirror  
**File:** `10-mirror_permissions`  
This script sets the mode of `hello` to be the same as `olleh`.

```bash
#!/bin/bash
chmod --reference=olleh hello
```

### 11. Directories  
**File:** `11-directories_permissions`  
This script adds execute permission to all subdirectories for everyone.

```bash
#!/bin/bash
chmod -R +X *
```

### 12. More directories  
**File:** `12-directory_permissions`  
This script creates a directory `my_dir` with `751` permissions.

```bash
#!/bin/bash
mkdir -m 751 my_dir
```

### 13. Change group  
**File:** `13-change_group`  
This script changes the group owner of `hello` to `school`.

```bash
#!/bin/bash
chgrp school hello
```

### 14. Owner and group  
**File:** `14-change_owner_and_group`  
This script changes the owner to `vincent` and the group owner to `staff` for all files and directories in the working directory.

```bash
#!/bin/bash
chown -R vincent:staff *
```

### 15. Symbolic links  
**File:** `15-symbolic_link_permissions`  
This script changes the owner and group of `_hello` (a symbolic link) to `vincent` and `staff`.

```bash
#!/bin/bash
chown -h vincent:staff _hello
```

### 16. If only  
**File:** `16-if_only`  
This script changes the owner of `hello` to `vincent` **only if** it is currently owned by `guillaume`.

```bash
#!/bin/bash
chown --from=guillaume vincent hello
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


