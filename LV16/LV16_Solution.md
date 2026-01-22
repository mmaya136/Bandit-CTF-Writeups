# Bandit Level 15 → Level 16
<img width="1100" height="375" alt="image" src="https://github.com/user-attachments/assets/49871e14-c16d-4594-b7d1-de4d615ed1fd" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit16**.

## Description
The challenge states that the password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost using SSL/TLS encryption**.

This means that a secure connection is required, and a normal plain-text connection will not work.

## Methodology
First, a secure SSL/TLS connection is established to **localhost on port 30001** using `ncat`.  
Once the connection is successfully established, the current password for **bandit15** is entered.  
If the password is correct, the server responds with the password for **bandit16**.

<img width="413" height="114" alt="image" src="https://github.com/user-attachments/assets/ad796dd7-6ceb-47c7-9d30-03c75bfa5b1a" />


## Commands Used
```bash
ncat localhosst 30001 --ssl



