# Bandit Level 14 → Level 15
<img width="909" height="431" alt="image" src="https://github.com/user-attachments/assets/e477306c-6c6d-4b0b-9279-69d9a0dc9b70" />
## Objective
The objective of this level is to obtain the password for the next level, **bandit15**.

## Description
The challenge states that the password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

A service is running locally and listening on this port. When the correct password is sent, the service responds with the password for the next level.

## Methodology
First, a connection is established to **localhost on port 30000** using `nc` (netcat).  
Once connected, the current password for **bandit14** is entered and sent to the service.  
If the password is correct, the server returns the password for **bandit15**.

<img width="395" height="81" alt="image" src="https://github.com/user-attachments/assets/b8c846b5-f62f-4217-8a68-1e9efd362a35" />


## Commands Used
```bash
nc localhost 30000
