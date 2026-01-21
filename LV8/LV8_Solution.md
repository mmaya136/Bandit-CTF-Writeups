# Bandit Level 7 → Level 8
<img width="916" height="251" alt="image" src="https://github.com/user-attachments/assets/a0382bc1-1d8e-4300-9b52-e53af98e4139" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit8**.

## Description
The challenge states that the password for the next level is stored in the file `data.txt`, next to the word **millionth**.

The file contains a large amount of text, so manually searching for the password is inefficient. A command-line search tool is required.

## Methodology
The `grep` command is used to search for the specific word **millionth** inside the `data.txt` file.  
Once the matching line is found, the password located next to that word is revealed.

<img width="539" height="849" alt="image" src="https://github.com/user-attachments/assets/1c9a9c61-09f6-447a-a9a1-0441c492575d" />

<img width="479" height="84" alt="image" src="https://github.com/user-attachments/assets/5dd80e6c-7579-44fd-b99f-20d93df270ea" />

## Commands Used
```bash
grep millionth data.txt



