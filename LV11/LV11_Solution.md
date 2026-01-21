# Bandit Level 10 → Level 11
<img width="567" height="244" alt="image" src="https://github.com/user-attachments/assets/95342fe0-2a1b-42aa-9ef3-6cc5034cc074" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit11**.

## Description
The challenge states that the password for the next level is stored in the file `data.txt`, which contains **Base64-encoded data**.

In order to retrieve the password, the encoded content must be decoded.

## Methodology
To solve this level, the contents of the `data.txt` file are decoded using the `base64` command.  
Once decoded, the plaintext output reveals the password for the next level.
<img width="567" height="90" alt="image" src="https://github.com/user-attachments/assets/03c50acb-55b4-4e96-82ad-c24ddf8f24a0" />


## Commands Used
```bash
cat data.txt | base64 -d



