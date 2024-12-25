## Approach :

1. First, copy the file and use `wget` to download it into your directory. We get a jpg file.

2. Opening it and checking the contents doesn't give us anything, but according to the clue we need to view information of the file.

3. For this purpose, we use the `exiftool` command, after using it we get the following results :

![image](https://github.com/user-attachments/assets/e8cd62ef-16be-4ccb-8b63-5e828f6e2c70)

4. In this case, the license seems to be a base32 or base64 encoded, hence I copied it and pasted it in a base64 decoder, which gives us the flag.

5. If you want to do it on the terminal, I copied the text and saved it in a file like this :

    ```bash
   echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" > flag.txt
    ```

    Then I decoded the file using :

   ```bash
   cat flag.txt| base64 -d
   ```
   
6. We get the flag :  `picoCTF{the_m3tadata_1s_modified}`


# Notes :
No matter the file, it's always recommended to use `exiftool` to check the contents once.
