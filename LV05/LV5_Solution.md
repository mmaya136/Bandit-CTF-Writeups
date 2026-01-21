# Bandit Level 4 → Level 5
<img width="1098" height="205" alt="image" src="https://github.com/user-attachments/assets/b292f298-778e-4f8b-8a04-9ca5ddb532d8" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit5**.

## Description
The challenge states that the password for the next level is stored in the **only human-readable file** inside the `inhere` directory.

The directory contains multiple files, most of which are not readable as plain text. The goal is to identify the file that contains human-readable content.

## Methodology
First, the `inhere` directory is accessed.  
Then, each file inside the directory is analyzed using the `file` command to determine its type.  
Once the human-readable file is identified, its contents are displayed to retrieve the password.

<img width="775" height="317" alt="image" src="https://github.com/user-attachments/assets/35dd379a-6715-4fd2-92ee-02b44b6c764f" />


## Commands Used
```bash
cd inhere
ls
file ./*
cat -- "-file07"


