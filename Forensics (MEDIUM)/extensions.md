# Approach

1. Download the file and use `exiftool` to check the information.
2. I see that the file is in a .txt format, but the details show that a .png file is stored inside it.
3. I used the command :

   ```bash
   mv file.txt file.png
   ```

4. This converted the file to a .png format, and then opening the file gives the flag.
5. The flag is  : `picoCTF{now_you_know_about_extensions}`


# Notes

1. Use `tesseract` to get the flag in another file, as this image had a big enough text for `tesseract` to recognise the text.
