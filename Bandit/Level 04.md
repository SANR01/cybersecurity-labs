# Bandit Level 4

## Objective
Find the only human-readable file in the directory and retrieve the password stored inside it.

## Initial Access
I was already logged into the Bandit system using SSH as the previous level user.

## Enumeration
I listed all files in the directory:

ls

I noticed multiple files with random names, so normal inspection was not enough.

## Challenge Faced
The main challenge was identifying which file contains readable content among multiple unknown/binary-like files.

A simple `cat` on each file was not efficient because most files were not readable in a meaningful way.

## Solution Approach
To solve this, I used the `file` command to check file types:

file *

This helped identify the human-readable file among all others.

After identifying the correct file, I read it using:

cat filename

## Result
The password for the next level was successfully retrieved from the identified human-readable file.

## Learning Outcome
- Learned how to use the `file` command for file type identification
- Understood importance of file analysis in enumeration phase
- Improved efficiency in handling multiple unknown files in Linux
