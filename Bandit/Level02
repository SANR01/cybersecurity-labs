# Bandit Level 2

## Objective
Access the file containing the password for the next level. The file has a non-standard name that includes spaces/special characters.

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

## Enumeration
I listed the files in the directory using:

ls

I noticed a file with a name that was not straightforward and contained spaces.

## Challenge Faced
The main issue was handling a filename that included spaces. Initially, a simple `cat filename` did not work because the shell interpreted the spaces as separate arguments.

## Solution Approach
To correctly access the file, I used quotation marks to handle the filename properly:

cat "filename"

This ensured the shell treated the entire string as a single file.

## Result
The file was successfully read and the content (password for the next level) was retrieved.

## Learning Outcome
- Learned how to handle filenames with spaces in Linux
- Understood importance of quoting in shell commands
- Improved command-line accuracy and attention to detail
