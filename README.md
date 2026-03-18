# Command Line Basics Assignment

**Course:** Cloud Computing - Basic Commands  
**Due Date:** February 15, 2026  
**Max Score:** 100

## Overview

This repository demonstrates basic Linux command line operations including directory creation, file manipulation, and text editing.

---

## Assignment Tasks Completed

### Task 1: Directory Structure Creation

**Objective:** Create a directory structure with a main `projects` folder containing `week1` and `week2` subfolders.

#### Commands Used:

```bash
# Create the main directory and subdirectories
mkdir -p projects/week1 projects/week2
```

**Explanation:**
- `mkdir`: Command to create directories
- `-p`: Creates parent directories as needed (projects, week1, week2)
- `projects/week1 projects/week2`: Creates both subdirectories in one command

#### Verification:

```bash
# List the directory structure
ls -R projects/

# Output:
# projects/:
# week1  week2
#
# projects/week1:
#
# projects/week2:
```

---

### Task 2: File Operations

#### Step 1: Create an empty file in week1

**Command:**
```bash
touch projects/week1/hello.txt
```

**Explanation:**
- `touch`: Creates an empty file or updates the timestamp of an existing file
- `projects/week1/hello.txt`: Path to the file to be created

**Verification:**
```bash
ls -la projects/week1/

# Output:
# total 8
# drwxr-xr-x 2 user user 4096 Feb 12 03:27 .
# drwxr-xr-x 4 user user 4096 Feb 12 03:27 ..
# -rw-r--r-- 1 user user    0 Feb 12 03:27 hello.txt
```

#### Step 2: Copy hello.txt to week2 and rename it

**Command:**
```bash
cp projects/week1/hello.txt projects/week2/hello_copy.txt
```

**Explanation:**
- `cp`: Command to copy files
- `projects/week1/hello.txt`: Source file
- `projects/week2/hello_copy.txt`: Destination path with new name

**Verification:**
```bash
ls -la projects/week2/

# Output:
# total 8
# drwxr-xr-x 2 user user 4096 Feb 12 03:27 .
# drwxr-xr-x 4 user user 4096 Feb 12 03:27 ..
# -rw-r--r-- 1 user user    0 Feb 12 03:27 hello_copy.txt
```

#### Step 3: Delete the original hello.txt from week1

**Command:**
```bash
rm projects/week1/hello.txt
```

**Explanation:**
- `rm`: Command to remove/delete files
- `projects/week1/hello.txt`: File to be deleted

**Verification:**
```bash
ls -la projects/week1/

# Output:
# total 8
# drwxr-xr-x 2 user user 4096 Feb 12 03:27 .
# drwxr-xr-x 4 user user 4096 Feb 12 03:27 ..
# (hello.txt is no longer present)
```

---

### Task 3: Create about_me.txt using vim

**Command:**
```bash
vim about_me.txt
```

**Vim Editor Steps:**
1. Press `i` to enter INSERT mode
2. Type your paragraph about motivation for learning Node.js
3. Press `Esc` to exit INSERT mode
4. Type `:wq` and press `Enter` to save and quit

**Alternative method using echo (command line):**
```bash
cat > about_me.txt << 'EOF'
My Motivation for Learning Node.js

I am motivated to learn Node.js because it offers a powerful and efficient 
way to build scalable server-side applications using JavaScript. As someone 
passionate about full-stack development, mastering Node.js will enable me to 
use the same language across both frontend and backend, streamlining my 
development workflow and deepening my understanding of the entire web 
application stack. The vast ecosystem of npm packages, the non-blocking I/O 
model, and the ability to handle concurrent connections make Node.js an 
essential skill for modern web development. I'm excited to leverage Node.js 
to build real-time applications, RESTful APIs, and microservices that can 
handle high traffic and provide seamless user experiences.
EOF
```

**Verification:**
```bash
cat about_me.txt
```

---

## Summary of Commands

| Command | Purpose |
|---------|---------|
| `mkdir -p` | Create directories (including parent directories) |
| `touch` | Create an empty file |
| `cp` | Copy files |
| `rm` | Remove/delete files |
| `ls -la` | List files with detailed information |
| `ls -R` | List files recursively |
| `vim` | Text editor for creating/editing files |
| `cat` | Display file contents |

---

## Additional Useful Commands

### Navigation Commands
```bash
pwd           # Print working directory
cd            # Change directory
cd ..         # Move up one directory
cd ~          # Go to home directory
```

### File Management
```bash
mv file1 file2        # Move or rename files
cp -r dir1 dir2       # Copy directories recursively
rm -r directory       # Remove directory and contents
mkdir directory       # Create a directory
rmdir directory       # Remove empty directory
```

### Viewing and Editing Files
```bash
cat file.txt          # Display entire file
less file.txt         # View file with scrolling
head file.txt         # Show first 10 lines
tail file.txt         # Show last 10 lines
nano file.txt         # Simple text editor
```

### File Information
```bash
ls -l                 # Long listing format
ls -a                 # Show hidden files
file filename         # Determine file type
stat filename         # Display file statistics
```

---

## Final Directory Structure

```
command-line-basics/
├── README.md
├── about_me.txt
└── projects/
    ├── week1/
    └── week2/
        └── hello_copy.txt
```

---

## Learning Outcomes

Through this assignment, I have learned to:
- Create and navigate directory structures using Linux commands
- Manipulate files (create, copy, rename, delete)
- Use command-line text editors
- Document my work using Markdown
- Version control using Git and GitHub

---

## Author

Paul Umeh  
Cloud Computing Course  
February 2026
