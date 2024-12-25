# Approach

1. Download the file. I used `exiftool` to check whether there is any hidden information, nothing was shown.
2. Then I ran `zsteg` to analyze the image, as this was a stegonography challenge. Turns out that there was a hidden zip file inside the .png file.

   ![image](https://github.com/user-attachments/assets/3e6d5430-3fe4-4215-9536-61f94a97fa8b)

3. Go to the secret directory and get the flag inside an image. The flag was :  `picoCTF{Hiddinng_An_imag3_within_@n_ima9e_82101824}`


# Notes

1. Don't use OCR tools that extract text from images to .txt files as it will give you a wrong output most of the time. Type the flag manually.
