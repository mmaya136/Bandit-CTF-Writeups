# Bandit Level 9 → Level 10
<img width="1050" height="249" alt="image" src="https://github.com/user-attachments/assets/ecaf14ab-818a-4bd2-a920-09d439f1f3a7" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit10**.

## Description
The challenge states that the password for the next level is stored in the file `data.txt`, inside one of the few **human-readable strings**, preceded by several `=` characters.

The file is not plain text, so standard text viewing commands are not sufficient.

## Methodology
To solve this level, the `strings` command is used to extract human-readable text from the file.  
Then, the output is filtered to locate strings preceded by `=` characters, which indicate the location of the password.

<img width="567" height="257" alt="image" src="https://github.com/user-attachments/assets/9a2e147f-5423-4902-bd82-95bfdae070bb" />
<img width="469" height="242" alt="image" src="https://github.com/user-attachments/assets/7f5018d4-11b6-4442-a202-7770842376ba" />




## Commands Used
```bash
strings data.txt | grep "="



