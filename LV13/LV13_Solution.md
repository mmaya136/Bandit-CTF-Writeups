# Bandit Level 12 → Level 13
## Objective
The objective of this level is to obtain the password for the next level, **bandit13**.

<img width="1677" height="338" alt="image" src="https://github.com/user-attachments/assets/3871d8bc-fd1d-44ba-b189-c06ea7ae3f84" />

## Description
The challenge states that the password for the next level is stored in the file `data.txt`, which is a **hexdump** of a file that has been **compressed multiple times using different formats**.

To solve this level, the hexdump must be converted back into a binary file and then decompressed step by step until the original file containing the password is recovered.

## Methodology
A temporary working directory is created to safely manipulate files.  
The hexdump is first reverted back into a binary file using `xxd`.  
Then, the file type is identified using the `file` command, and the appropriate decompression tool is applied.

This process is repeated until the final readable file is obtained.

<img width="567" height="596" alt="image" src="https://github.com/user-attachments/assets/11f81bc1-e36e-48a6-affb-e4e0c1c60d5e" />

<img width="450" height="104" alt="image" src="https://github.com/user-attachments/assets/feb72b76-318e-4dd2-b372-1c1902802387" />

<img width="1163" height="156" alt="image" src="https://github.com/user-attachments/assets/abcbb603-e234-4672-88ae-163a6bfe4df8" />


<img width="1020" height="82" alt="image" src="https://github.com/user-attachments/assets/82da646a-3472-4713-880e-ccde0b941182" />


<img width="1018" height="521" alt="image" src="https://github.com/user-attachments/assets/0c2b039c-8982-4d04-90f1-40c1fdf3f41c" />




## Commands Used
```bash
xxd -r data.txt > data
file data

mv data data.gz
gzip -d data.gz

mv data data.bz2
bzip2 -d data.bz2

mv data data.tar
tar -xf data.tar

mv data data.gz
gzip -d data.gz

