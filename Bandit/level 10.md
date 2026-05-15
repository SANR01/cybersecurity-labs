# Bandit Level 10

## Objective
Decode the encoded data inside the file to retrieve the password for the next level.

---

## Initial Access
I was already logged into the Bandit system via SSH as the previous level user.

---

## Enumeration
I listed the available files in the directory:

ls -la

A data file was present containing encoded text instead of plain readable information.

---

## Challenge Faced
The file content was encoded, so directly reading it with `cat` did not reveal the actual password.

The challenge was identifying the encoding format and properly decoding the data.

---

## Solution Approach
I first inspected the file content:

cat filename

The text appeared to be Base64 encoded.

To decode the content, I used the following command:

base64 -d filename

This converted the encoded data into readable plaintext and revealed the required password.

---

## Result
The encoded content was successfully decoded and the password for the next level was retrieved.

---

## Learning Outcome
- Learned how Base64 encoding works
- Practiced decoding encoded data in Linux
- Improved understanding of data transformation techniques
- Gained exposure to concepts commonly used in cybersecurity and data handling
