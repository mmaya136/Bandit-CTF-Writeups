# Bandit Level 16 → Level 17
<img width="1640" height="356" alt="image" src="https://github.com/user-attachments/assets/54cd9e19-65cc-4714-a005-e5a67a990411" />

## Objective
The objective of this level is to obtain the credentials for the next level, **bandit17**.

## Description
The challenge states that the credentials for the next level can be retrieved by submitting the password of the current level to a port on **localhost in the range 31000 to 32000**.

First, it is necessary to identify which ports in this range are open and listening.  
Then, determine which of these ports use **SSL/TLS**, since only one server will return the correct credentials.  
The remaining servers will simply echo back any input.

## Methodology
First, a port scan is performed on **localhost** to identify open ports in the range **31000–32000**.  
Next, each open port is tested to determine whether it supports **SSL/TLS**.  
Once the SSL/TLS-enabled port is found, a secure connection is established using `ncat`.  
Finally, the current password for **bandit16** is submitted to retrieve the credentials for **bandit17**.

<img width="666" height="187" alt="image" src="https://github.com/user-attachments/assets/a2d40915-1089-497b-9659-1aa17320138d" />

<img width="753" height="466" alt="image" src="https://github.com/user-attachments/assets/702483aa-bf38-4cc8-ac21-f24f778c0882" />

<img width="607" height="491" alt="image" src="https://github.com/user-attachments/assets/9c807ddb-0e64-4d35-b4c1-83d86484d68e" />




## Commands Used
```bash
nmap -p 31000-32000 localhost
nmap localhost -p 31000-32000  --script ssl-cert
ncat localhost 31790 --ssl

