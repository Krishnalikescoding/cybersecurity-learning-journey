# Cryptography Lab: Decrypting Files with Linux Commands

## Overview

This lab is a walkthrough of a Qwiklabs exercise on basic cryptography using Linux commands. It builds on earlier concepts of **encryption** and **decryption**, and the **Caesar cipher** — one of the earliest cryptographic algorithms used to protect data privacy.

As a security analyst, understanding how encryption secures data — and which security controls apply — is a core skill.

**Goal:** Use Linux commands to break a Caesar cipher and decrypt files to reveal hidden messages.

## Scenario

All files in the home directory have been encrypted. The task is to use Linux commands to:

1. Break the Caesar cipher protecting a hidden file.
2. Use the revealed command to decrypt the main data file.
3. Recover and read the hidden message.

**Starting point:** Logged in as user `analyst`, with `/home/analyst` as the current working directory.

## Task 1: Read the Contents of a File

**Goal:** Explore the home directory and read a file for further instructions.

1. List the files in the current working directory:
   ```bash
   ls
   ```
   Output shows two files — `Q1.encrypted` and `README.txt` — and one subdirectory, `caesar`.

2. Read the contents of `README.txt`:
   ```bash
   cat README.txt
   ```

**Result:** The `README.txt` file states that the `caesar` subdirectory contains a hidden file. This hidden file must be found and decrypted before recovering the main data.

## Task 2: Find and Decrypt the Hidden File

**Goal:** Locate the hidden file in the `caesar` subdirectory and solve the Caesar cipher inside it.

1. Change into the `caesar` subdirectory:
   ```bash
   cd caesar
   ```

2. List all files, including hidden ones:
   ```bash
   ls -a
   ```

   **Hidden files:** In Linux, hidden files are identified by a filename that starts with a period (`.`).

3. View the contents of the hidden file `.leftShift3`:
   ```bash
   cat .leftShift3
   ```

   The output looks scrambled because it has been encrypted with a **Caesar cipher** — each letter is shifted by a fixed number of positions in the alphabet. Here, the shift is **3 letters to the left**, so `d` represents `a`, `e` represents `b`, and so on.

4. Decrypt the Caesar cipher using the `tr` command:
   ```bash
   tr "d-za-cD-ZA-C" "a-zA-Z" < .leftShift3
   ```

   **`tr` command:** Translates text from one character set to another based on a mapping. The first parameter is the input character set; the second is the output character set. For example, mapping `"abcd"` → `"pqrs"` on input `"ac"` produces `"pr"`.

   In this case, `"d-za-cD-ZA-C"` (the shifted alphabet) is mapped back to `"a-zA-Z"` (the normal alphabet), reversing the shift.

   **Result:** The decrypted output reveals the exact command needed for Task 3.

5. Return to the home directory:
   ```bash
   cd ~
   ```

## Task 3: Decrypt the Data File

**Goal:** Use the command revealed in Task 2 to decrypt `Q1.encrypted` and recover the hidden message.

1. Run the decryption command revealed by the Caesar cipher:
   ```bash
   openssl enc -aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
   ```

   **Command breakdown:**

   | Option | Meaning |
   |---|---|
   | `enc` | Invokes OpenSSL's encoding/decoding function |
   | `-aes-256-cbc` | Specifies the symmetric cipher used (AES-256 in CBC mode) |
   | `-pbkdf2` | Adds extra security by strengthening the key derivation |
   | `-a` | Specifies base64 encoding for input/output |
   | `-d` | Indicates decryption (as opposed to encryption) |
   | `-in Q1.encrypted` | Specifies the input (encrypted) file |
   | `-out Q1.recovered` | Specifies the output (decrypted) file |
   | `-k ettubrute` | Specifies the password used for decryption |

2. Confirm the new file was created:
   ```bash
   ls
   ```
   A new file, `Q1.recovered`, now appears — this is the decrypted file.

3. Read the recovered message:
   ```bash
   cat Q1.recovered
   ```

### Example

Running this workflow end-to-end demonstrates a full **decrypt-the-decryptor** chain: a hidden file encrypted with a simple Caesar cipher contains the exact `openssl` command needed to decrypt a separate, more securely encrypted file (AES-256-CBC).

## Caesar Cipher vs. AES-256-CBC

| Caesar Cipher | AES-256-CBC |
|---|---|
| Simple substitution cipher — shifts each letter by a fixed number of positions | Modern symmetric-key block cipher using a 256-bit key |
| Easily broken by brute force or frequency analysis | Computationally secure against brute-force attacks |
| No key management, encoding, or password required | Requires a key/password and supports key-strengthening (e.g., `-pbkdf2`) |
| Used here for a simple hidden-message puzzle | Used here to protect the actual data file |

## Conclusion

This lab provided practical experience with basic Linux Bash shell commands to:

- List hidden files (`ls -a`)
- Decrypt a Caesar cipher (`tr`)
- Decrypt an AES-256-CBC encrypted file (`openssl`)

This exercise is a foundational step toward understanding how encryption and decryption work in practice.