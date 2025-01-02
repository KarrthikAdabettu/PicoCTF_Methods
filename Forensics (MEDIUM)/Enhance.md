# Approach

1. Download the file. I used `exiftool` to check information on the photo.
2. I found that it's a SVG + XML text, which hinted that the flag might be in the binary coded text.
3. I ran the file through `strings` and got the text.
4. While checking it, what was interesting was that every line in the last part of the text was the letter for the flag picoCTF.


   ![image](https://github.com/user-attachments/assets/b5c63029-8605-4b4f-9716-1a5ec2c5ca83)



5. I manually copied the text and found the flag.


# Notes

None.

