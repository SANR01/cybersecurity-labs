# Bandit Level 11

## Objective
Decode the text that has been encrypted using ROT13 encoding in order to retrieve the password for the next level.

---

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

---

## Enumeration
I checked the available files in the current directory:

ls -la

A data file was present containing encoded text that was not immediately understandable.

---

## Challenge Faced
The file content appeared scrambled but still consisted of readable alphabetic characters.

The challenge was identifying the encoding technique used and finding a way to decode it efficiently.

---

## Solution Approach
After analyzing the text pattern, I identified it as ROT13 encoding.

To decode the content, I used the `tr` command:

cat filename | tr 'A-Za-z' 'N-ZA-Mn-za-m'

This rotated the characters back to their original form and revealed the password.

---

## Result
The encoded message was successfully decoded and the password for the next level was retrieved.

---

## Learning Outcome
- Learned how ROT13 encoding works
- Practiced character transformation using the `tr` command
- Improved understanding of simple encoding/obfuscation techniques
- Gained exposure to text manipulation in Linux
