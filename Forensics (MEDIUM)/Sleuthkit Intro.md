# Approach

1. Download the file and `gunzip` the .gz file. I see the disk image and thought of using `autopsy` instead of `mmls` as I didn't have much knowledge on it.
2. After a lot of digging through files, I couldn't find anything and decided to check out `mmls`.
3. To my surprise, it's just a command used to list the partition table contents so that you can determine where each partition starts. Using that on the image gave the following details :

   ![image](https://github.com/user-attachments/assets/05e92894-69af-4c4b-bebb-61b2d10a1880)

4. Then just use the command from the challenge and enter the password, which is the length of Linux displayed on screen.
5. The flag for the challenge tunred out to be :  `picoCTF{mm15_f7w!}`
