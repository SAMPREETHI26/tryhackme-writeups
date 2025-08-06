# John the Ripper: The Basics 🛡️

Welcome to my write-up for the **"Hash Cracking"** room on TryHackMe. This room introduces key cryptographic concepts and demonstrates how to crack hashes using one of the most powerful tools in cybersecurity: **John the Ripper**.

---

## ♟️ Take Aways

- What are hashes, and why are they important?
- Why hashes are considered "one-way" functions
- How password hashes can be cracked using dictionary attacks
- How to use **John the Ripper** for hash cracking
💡 Note: This write-up starts from Task 4, where the actual hands-on usage of the John the Ripper tool begins. Earlier tasks cover theory or setup steps, but Task 4 onwards dives into practical password cracking exercises.

---

##  ♟️ What is a Hash?
 A **hash** is a fixed-length string generated from data of any size using a **hashing algorithm**. Hashes are used to **protect sensitive information** like  passwords by masking the original value.
Features:
-  One-way (can’t be reversed)
-  Fixed in size (regardless of input)
-  Unique (small changes produce completely different hashes)
  
---
## ♟️ Why are hashes secure?
Hashes are considered secure because they are one-way functions—easy to compute but nearly impossible to reverse. 
Even a small change in input produces a completely different output, making it hard for attackers to guess the original data.

## ♟️ Dictonary attacks

> Take a wordlist of possible passwords

> Hash each one

> Compare it to the target hash

> If a match is found — password cracked ✅

## ♟️ rockyou.txt
rockyou.txt is a popular wordlist file that contains millions of common passwords. It’s often used in password-cracking tools like John the Ripper to guess weak passwords during dictionary attacks.

## ♟️ John The Ripper
John the Ripper is a tool used to crack passwords by guessing them from a list of common passwords. It supports dictionary, brute-force, and hybrid attacks across various hash types.

## ♟️ Task 4 : Cracking Basic Hashes

1 . what type of hash is hash1.txt?
    To identify hash type 🔍
    > Navigate to the task04 directory.
    > use the command below to get the contents of the file
      ```bash
      cat hash1.txt 
    > note down the hash value
    > use the command python3 hash-id.py , provide the hash value that was previously noted , 
      as you can see from below , we can say that the type of hash is md5
      ![Alt Text](images/hash-output.png)






