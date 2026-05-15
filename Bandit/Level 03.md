# Bandit Level 3

## Objective
Locate and retrieve the password from a hidden file inside the directory.

## Initial Access
I was already logged into the Bandit system as the previous level user via SSH.

## Enumeration
I used the following command to list all files, including hidden ones:

ls -a

I noticed a hidden directory named `.hidden`.

## Challenge Faced
The main challenge was identifying hidden files and understanding that important data is not always visible using a normal `ls` command.

## Solution Approach
I navigated into the hidden directory and checked its contents:

cd .hidden  
ls  
cat filename

The password file was successfully located and read.

## Result
The required password for the next level was retrieved successfully from the hidden file.

## Learning Outcome
- Learned how to identify hidden files and directories in Linux
- Understood the importance of `ls -a` for enumeration
- Improved awareness of Linux file system behavior
