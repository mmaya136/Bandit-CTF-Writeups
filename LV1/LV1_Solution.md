
# Bandit Level 0 → Level 1
<img width="1631" height="358" alt="image" src="https://github.com/user-attachments/assets/e9f5fdf1-bc1a-4cda-8fe0-2b487cb3b57e" />

## Objective
The goal of this level is to obtain the password for the next level, **bandit1**.

## Description
The challenge states that the password for the next level is stored in a file named `readme`, located in the home directory of the current user. Once the password is found, it must be used to log in to the next level via SSH on port `2220`.

## Methodology
To solve this level, basic Linux commands are sufficient. The approach consists of locating the `readme` file in the home directory and displaying its contents to retrieve the password.


## Commands Used
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme

password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If






