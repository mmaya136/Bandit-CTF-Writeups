<img width="681" height="253" alt="image" src="https://github.com/user-attachments/assets/07bf4bdd-7117-48c0-9a77-e2029172003f" /># Bandit Level 3 → Level 4
<img width="571" height="184" alt="image" src="https://github.com/user-attachments/assets/8209c2fb-50c4-4629-a5b0-14f72dd49476" />

## Objective
The objective of this level is to obtain the password for the next level, **bandit4**.

## Description
The challenge states that the password for the next level is stored in a **hidden file** located inside the `inhere` directory.

Hidden files in Linux start with a dot (`.`), so they are not displayed by default when listing directory contents.

## Methodology
First, the `inhere` directory is accessed.  
Then, the contents of the directory are listed using the `-a` option to include hidden files.  
Once the hidden file is identified, its contents are displayed to retrieve the password.
<img width="681" height="253" alt="image" src="https://github.com/user-attachments/assets/f554878a-2b92-4fd0-ab02-20f0745ae621" />

## Commands Used
```bash
cd inhere
ls -la
cat ...Hiding-From-You




