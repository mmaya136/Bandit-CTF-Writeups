# Bandit Level 17 → Level 18
<img width="1482" height="259" alt="image" src="https://github.com/user-attachments/assets/e960252a-a344-4ec1-ad53-b1e6ac12e6d4" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit18**.

## Description
The challenge states that there are two files in the home directory: **passwords.old** and **passwords.new**.  
The password for the next level is located in **passwords.new** and is the **only line that differs** between the two files.

By comparing both files, the changed line can be identified, which corresponds to the password for the next level.

## Methodology
First, the contents of the home directory are listed to confirm the presence of both files.  
Then, the `diff` command is used to compare **passwords.old** and **passwords.new**.  
The output shows the single modified line, which contains the password for **bandit18**.

<img width="460" height="173" alt="image" src="https://github.com/user-attachments/assets/2dda1c16-db9d-46eb-8b86-94dd34ada887" />


## Commands Used
```bash
diff passwords.old passwords.new



