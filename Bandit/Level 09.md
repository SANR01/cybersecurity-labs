# Bandit Level 9

## Objective
Retrieve the password hidden inside a file containing mostly non-human-readable (binary) data.

---

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

---

## Enumeration
I listed the files in the current directory:

ls -la

A data file was present, but opening it normally displayed unreadable and corrupted-looking characters.

---

## Challenge Faced
The main challenge was that the file contained binary/non-readable content, making normal viewing commands like `cat` ineffective.

Most of the output contained random symbols and unreadable text.

---

## Solution Approach
To extract readable strings from the file, I used the `strings` command:

strings filename

Since the password was associated with a specific keyword/pattern, I combined it with `grep`:

strings filename | grep "keyword"

This filtered the readable output and revealed the required credential.

---

## Result
The hidden password was successfully extracted from the binary data.

---

## Learning Outcome
- Learned how to analyze binary/non-readable files
- Understood usage of `strings` command
- Improved pattern filtering using `grep`
- Gained basic exposure to data extraction techniques used in forensics and malware analysis
