
# Bandit Level 13 → Level 14
<img width="1663" height="306" alt="image" src="https://github.com/user-attachments/assets/00ac74df-8b09-4cff-9178-ecdd38ee45e4" />

## Objective
The objective of this level is to obtain access to the next level, **bandit14**.

## Description
The challenge states that the password for the next level is stored in  
`/etc/bandit_pass/bandit14` and can only be read by user **bandit14**.

Instead of receiving the password directly, this level provides a **private SSH key** that must be used to authenticate as `bandit14`.

## Methodology
First, the home directory is inspected to locate the provided private SSH key.  
Once identified, proper file permissions are applied to the key to ensure it can be used by SSH.

Then, the SSH client is used with the `-i` option to authenticate using the private key and log in as `bandit14`.

<img width="567" height="440" alt="image" src="https://github.com/user-attachments/assets/acf74248-6921-4226-806e-81a1adff192e" />
<img width="567" height="113" alt="image" src="https://github.com/user-attachments/assets/642f5a66-6e98-44f3-a899-82f6b8a232ab" />
<img width="453" height="60" alt="image" src="https://github.com/user-attachments/assets/9867f7bc-c196-4e97-9e80-880e83b04fbb" />


## Commands Used
```bash
ls
cat sshkey.private
chmod 600 sshkey.private
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
