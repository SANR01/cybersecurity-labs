# Bandit Level 7

## Objective
Find the password stored in a specific file by searching for a known keyword within a large file.

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

## Enumeration
I listed the files in the directory:

ls -la

I found a file containing a large amount of text data, making manual search inefficient.

## Challenge Faced
The challenge was:
- File contained a large number of lines
- Password was not immediately visible
- Manual reading was not practical

## Solution Approach
To efficiently locate the required information, I used the `grep` command:

grep "keyword" filename

This helped me filter out the exact line containing the required password.

Alternatively, I could also use:

cat filename | grep "keyword"

## Result
The correct line containing the password was successfully identified and extracted.

## Learning Outcome
- Learned how to use `grep` for pattern searching
- Understood importance of log/data filtering in Linux
- Improved efficiency in handling large files
- Learned real-world SOC-style data analysis technique
