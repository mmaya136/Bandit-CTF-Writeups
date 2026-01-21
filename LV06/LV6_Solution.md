# Bandit Level 5 → Level 6
<img width="924" height="295" alt="image" src="https://github.com/user-attachments/assets/c647e520-198d-48a2-986e-482b1473691e" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit6**.

## Description
The challenge states that the password for the next level is stored in a file somewhere under the `inhere` directory.  
The file has the following properties:
- Human-readable
- Exactly 1033 bytes in size
- Not executable

## Methodology
First, the search is limited to the `inhere` directory.  
Then, the `find` command is used with specific filters to locate files that match the given properties.  
Once the correct file is identified, its contents are displayed to retrieve the password.

<img width="1152" height="256" alt="image" src="https://github.com/user-attachments/assets/ea05ae23-a2c0-4270-bee8-ae106a2bcbd9" />


## Commands Used
```bash
cd inhere
find . -type f -size 1033c ! -executable
cat ./maybehere07/.file2



