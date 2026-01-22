# Bandit Level 18 → Level 19
<img width="1175" height="233" alt="image" src="https://github.com/user-attachments/assets/b89ef980-96e8-46dd-b762-6aecc9e36be4" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit19**.

## Description
The challenge states that the password for the next level is stored in a file called **readme** in the home directory.  
However, the `.bashrc` file has been modified to automatically log the user out when logging in via SSH, preventing normal interaction.

To solve this, a command must be executed directly when establishing the SSH connection, bypassing the logout behavior.

## Methodology
Instead of starting an interactive shell, an SSH connection is made while directly executing a command.  
By doing so, the `.bashrc` file is not executed, allowing access to the **readme** file.  
The contents of the file are then displayed to retrieve the password for **bandit19**.

<img width="501" height="176" alt="image" src="https://github.com/user-attachments/assets/1a57e657-30fa-47bd-a42b-707d111f0f7d" />

<img width="693" height="303" alt="image" src="https://github.com/user-attachments/assets/d1b469a2-e763-4f19-abca-dbe67b5dfa9b" />

<img width="617" height="290" alt="image" src="https://github.com/user-attachments/assets/a64792e4-ffff-4c00-975c-d342a3785b64" />




## Commands Used
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
