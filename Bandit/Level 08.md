# Bandit Level 8

## Objective
Identify the unique line in a file where all other lines are repeated multiple times.

---

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

---

## Enumeration
I listed the files in the directory:

ls -la

A data file containing many repeated lines was present.

---

## Challenge Faced
The file contained a large amount of duplicated data, making it difficult to manually identify the correct unique value.

Simply reading the file with `cat` was not practical because the output was too repetitive.

---

## Solution Approach
To solve this efficiently, I used sorting and duplicate filtering commands together:

sort filename | uniq -u

Explanation:
- `sort` organizes identical lines together
- `uniq -u` displays only the unique line

This allowed me to quickly isolate the required password.

---

## Result
The unique line containing the password was successfully identified.

---

## Learning Outcome
- Learned how to use `sort` and `uniq`
- Understood importance of command pipelines (`|`)
- Improved Linux data processing and filtering skills
- Learned efficient handling of repetitive data in terminal environments
