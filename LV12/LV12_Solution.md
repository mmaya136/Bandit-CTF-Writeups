# Bandit Level 11 → Level 12
<img width="1022" height="308" alt="image" src="https://github.com/user-attachments/assets/7b6d67f9-4b1e-45e2-8fe2-0bba4c03727d" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit12**.

## Description
The challenge states that the password for the next level is stored in the file `data.txt`, where all lowercase (`a-z`) and uppercase (`A-Z`) letters have been rotated by **13 positions**.

This encoding method is known as **ROT13**, a simple letter substitution cipher.

## Methodology
To solve this level, the contents of the `data.txt` file are decoded using the `tr` command to apply a ROT13 transformation.  
Both lowercase and uppercase letters must be translated back to their original positions.

<img width="554" height="131" alt="image" src="https://github.com/user-attachments/assets/6d66aa4b-ba8f-4384-b6b4-18d7456b338f" />


## Commands Used
```bash
cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'



