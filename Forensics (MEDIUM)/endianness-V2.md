# Approach

1. Download the file from the challenge, here there wasn't any extension to the file.
2. I used `exiftool` to check out the information regarding the file, and found out that it is supposed to be a jpeg file.

   ![image](https://github.com/user-attachments/assets/35302c4f-1f94-4055-ae68-7c7eca5d85a3)

3. Opening the file using `hexeditor`, we get the following image, which shows us that it's a JPEG image but in the little endian version.

   ![image](https://github.com/user-attachments/assets/8aa106ad-9c9f-48bc-b7db-0eb76cf89dad)

4. We need to convert it into the big endian system, which can be achieved by reversing the bits by 4 places. This is the place where I got stuck, as there were no tools online where we could upload the entire file and it gave us a new file with the reversed bits.
5. I looked up several approaches, among those many used a custom python script that reversed the bits in the file to get the proper file. Here, I found that [NoamGariani11](https://github.com/noamgariani11)'s approach was the easiest, hence will link the repo here. Basically we go to this site : [CyberChef - Swap Endianness and Render Image](https://gchq.github.io/CyberChef/#recipe=To_Hex('Space',0)Swap_endianness('Hex',4,true)From_Hex('Auto')Render_Image('Raw')) and upload the file, which gives us the following image with the flag :

![image](https://github.com/user-attachments/assets/0be5c7fe-ab41-4ce6-920c-40076fbc22cf)

6. The flag is :  `picoCTF{cert!f1Ed_iNd!4n_s0rrY_3nDian_f72c4bf7}`



# Credits

I found [NoamGariani11](https://github.com/noamgariani11)'s approach to be the best one here. I am also linking some other people's approaches as I found those to be quite good as well.

[Endianness v2 Challenge Solve - PicoCTF 2024 by 0xVirtu4l](https://medium.com/@0xVirtu4l/picoctf-2024-endianness-v2-challenge-solve-f9c93d6b8fa6)

[PicoCTF 2024 Endianness v2 by Shreethaar](https://medium.com/@shreethaar/picoctf-2024-endianness-v2-8e41857f6adb)



# Notes

Learning how little endian and big endian works is the key to this problem.




