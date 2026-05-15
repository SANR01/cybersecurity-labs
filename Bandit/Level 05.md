# Bandit Level 5

## Objective
Find the file that meets specific conditions (human-readable, not executable, and of a certain size) and retrieve the password from it.

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

## Enumeration
I first listed all files and subdirectories:

ls

Since there were multiple files, manual checking was not efficient.

## Challenge Faced
The challenge was to identify the correct file based on specific properties:
- Human-readable
- Not executable
- Specific file size requirement

Normal `ls` was not enough to filter these conditions.

## Solution Approach
To solve this efficiently, I used the `find` command with conditions:

find . -type f -size <required_size>

This helped narrow down the correct file.

After identifying the file, I verified its content using:

file filename  
cat filename

## Result
The correct file was identified successfully and the password for the next level was retrieved.

## Learning Outcome
- Learned how to use `find` command with filters
- Understood file properties like size and permissions
- Improved efficient enumeration techniques in Linux
