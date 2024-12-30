# Approach

1. Download the file. I used `exiftool` to check whether there is any hidden information, nothing was shown.
2. Then I ran `zsteg` to analyze the image, right then and there I got the flag mentioned with the $3tg0 ending mentioned in the hint.

   ![image](https://github.com/user-attachments/assets/c50323e7-9d7a-4986-bf0e-526d3f439336)


3. I tried checking the same thing with `strings` but it didn't yield results.


# Notes

1. For most stegonography challenges use `zsteg` or `steghide` before trying any other tool, as these are the most common and easy ones.
