## Approach :

1. First, copy the file and use `wget` to download it into your directory. Then, unzip the folder.

2. We see a jpg file. Opening it and checking the contents doesn't give us anything, but according to the clue we need to view information of the file.

3. For this purpose, we use the `exiftool` command, after using it we get the following results :

![image](https://github.com/user-attachments/assets/843461e4-7ad4-4b95-8b70-6ca56e5d4f92)

4. If we look closely, the attribution URL seems to be a base32 or base64 encoded, hence I copied the URL and pasted it in a base64 decoder, which gives us the flag.

5. If you want to do it on the terminal, I copied the URL and saved it in a file like this :

    ```bash
    echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==" > flag.txt
    ```

    Then I decoded the file using :

   ```bash
   cat flag.txt| base64 -d
   ```
   
6. We get the flag :  `picoCTF{ME74D47A_HIDD3N_6a9f5ac4}`


# Notes :
No matter the file, it's always recommended to use `exiftool` to check the contents once.
