# Approach

1. Download the disk image. Use `gunzip` to extract the disk image.
2. Use `autopsy` to analyze the disk image.
3. You will find the following files :

  ![image](https://github.com/user-attachments/assets/ffd7b5fc-3d4f-4ce4-acf2-6c7c98efdcc2)

4. From autopsy, download the "id_ed25519" file into your directory.
5. Now in another terminal, use the `ssh -i...` command you got from launching the instance. Instead of the key_file, replace it with the id_ed25519 file.
6. It was asking me for a password for a long time, and I tried everything I could but couldn't figure anything out. Hence I went to look for some help, I finally found
   my answer in this video : -[Almond Force](https://www.youtube.com/watch?v=fGWdueqArzE&t=259s)
   
7. The problem I was facing was, the file had only permissions set so that the owner can do read, write and execute. We had to change the permissions, hence I used :

   ```bash
   chmod 600 id_ed25519
   ```

8. After changing the permissions and logging in, you can get the flag by using `cat`.
9. The flag is :  `picoCTF{k3y_5l3u7h_339601ed}`


# Notes

1. Make sure to download the file if you're using `autopsy`.
