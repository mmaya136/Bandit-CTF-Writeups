# Bandit Level 8 → Level 9
<img width="771" height="308" alt="image" src="https://github.com/user-attachments/assets/578c563a-1583-4c5a-a1a3-0ddeb614ab76" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit9**.

## Description
The challenge states that the password for the next level is stored in the file `data.txt` and is the **only line of text that occurs exactly once**.

The file contains many repeated lines, so identifying the unique line requires processing the data rather than reading it manually.

## Methodology
To solve this level, the file contents are first sorted so that identical lines are grouped together.  
Then, the `uniq` command is used to identify the line that appears only once.
This is achieved by combining commands using pipes.
 <img width="509" height="667" alt="image" src="https://github.com/user-attachments/assets/cad11cf8-0dc0-421e-9b31-bcd2237a1b11" />










<img width="367" height="62" alt="image" src="https://github.com/user-attachments/assets/cd2d0f74-8380-497c-a384-cc2747665d12" />



## Commands Used
```bash
sort data.txt | uniq -u




