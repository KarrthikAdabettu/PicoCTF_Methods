# Approach

1. Download the file, we get a png file which upon opening is corrupted.
2. From the challenge, we can see that it's a stegonography challenge, meaning that the flag is hidden between the bits of the image. The reason for the corruption of the image is that there is a flag somewhere causing the corruption.
3. My initial response was using the tool `zsteg`, which is very similar to `strings` but it gives out all the data of the image's LSB and MSB as shown below :

   ![image](https://github.com/user-attachments/assets/59c4f1a7-7516-490f-9885-97f1eff7f570)
   
4. After this, I thought of using `steghide`, but decided not to as it's the same as `zsteg` and also asks for a password.
5. I then found `stegsolve`, which is a java program that will simplify the process of finding hidden data in images. The link to download stegsolve is given below :

   [Process to Install StegSolve by Manisashank](https://github.com/manisashank/stegsolve/blob/master/process%20to%20install%20stegsolve)

6. After installing, use the following command to execute it :
   
```bash
java -jar stegsolve.jar
```

It opens an interface where you import the png file. Then go to the analyze option and click on "Data Extract", since we know that the image has passed LSB statistical analysis, we need to focus on the MSB. 

![image](https://github.com/user-attachments/assets/ba34d397-bbb4-48d9-ae14-124bf822ec45)

7. We get the hex dump extracted text, now save that file in your directory. Use a text editor like `subl` or `nano` and search for the flag.

   ![image](https://github.com/user-attachments/assets/465b2a78-09ed-4645-9390-1a4352c0297a)
   

9. The flag we get is :  `picoCTF{15_y0ur_que57_qu1x071c_0r_h3r01c_ea7deb4c}`


# Notes

1. Make sure to remove the spaces from the flag text.
2. There is another method to solve this using `sigBits.py`, but I'm not too sure how to use that.
