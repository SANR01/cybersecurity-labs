# Bandit Level 6

## Objective
Find the file that contains the password based on specific conditions such as:
- Owned by a specific user/group
- Specific size
- Not readable directly through normal directory listing

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

## Enumeration
I started by listing all files and directories:

ls -la

Since multiple files and directories were present, I needed a more advanced approach to locate the correct file.

## Challenge Faced
The challenge was that the target file:
- Was not easily identifiable by name
- Required filtering based on ownership and permissions
- Could not be found using basic `ls` or manual checking

## Solution Approach
I used the `find` command with ownership and permission filters:

find / -user bandit7 -group bandit6 -size <required_size> 2>/dev/null

This helped me locate the exact file that matched the required conditions.

After finding the file path, I read its content:

cat /path/to/file

## Result
The correct file was identified and the password for the next level was successfully retrieved.

## Learning Outcome
- Learned how to use `find` with user and group filters
- Understood Linux file ownership concepts
- Learned how to suppress permission errors using `2>/dev/null`
- Improved real-world enumeration skills for VAPT scenarios
