# Bandit Level 6 → Level 7
<img width="922" height="276" alt="image" src="https://github.com/user-attachments/assets/1c68f66c-1548-4592-9af1-48e5e81b7ae3" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit7**.

## Description
The challenge states that the password for the next level is stored **somewhere on the server** and has the following properties:
- Owned by user `bandit7`
- Owned by group `bandit6`
- Exactly 33 bytes in size

Because the file is not restricted to a specific directory, a full system search is required.

## Methodology
The `find` command is used to search the entire filesystem while filtering by file owner, group, and size.  
Since searching the whole system generates many permission errors, standard error output is redirected to `/dev/null` to keep the output clean.

Once the correct file is found, its contents are displayed to retrieve the password.

<img width="1896" height="236" alt="image" src="https://github.com/user-attachments/assets/175e87e1-9d3b-461c-95fe-0e62fc7bb98e" />

## Commands Used
```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password




